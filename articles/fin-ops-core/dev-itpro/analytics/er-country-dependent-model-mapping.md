---
title: 国コンテキスト依存の ER モデル マッピングのコンフィギュレーション
description: このトピックでは、使用を制御する法人の国/地域コンテキストによって異なる、ER モデル マッピングを設定する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 6c4b18a3cf2ba313756d5f761ef1beb2c3015516
ms.sourcegitcommit: 56add4c49c35c65a75fa2ca5234927e7f7cd66ef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/11/2019
ms.locfileid: "2781148"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a><span data-ttu-id="2f7f1-103">国コンテキスト依存の ER モデル マッピングのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2f7f1-103">Configure country context dependent ER model mappings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2f7f1-104">電子申告 (ER) モデル マッピングをコンフィギュレーションして、一般的な ER データ モデルを実装しますが、Dynamics 365 Finance に固有のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-104">You can configure Electronic reporting (ER) model mappings so that they implement a generic ER data model but are specific to Dynamics 365 Finance.</span></span> <span data-ttu-id="2f7f1-105">このトピックでは、ER データ モデルに複数の ER モデル マッピングを設計して、異なる国/地域コンテキストがある会社から実行される対応する ER 形式によってどのように使用されるかを制御する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-105">This topic explains how to design multiple ER model mappings for an ER data model to control how they are used by corresponding ER formats that are run from companies that have different country/region contexts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2f7f1-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="2f7f1-106">Prerequisites</span></span>

<span data-ttu-id="2f7f1-107">このトピックの例を完了するには、次のアクセスが必要です:</span><span class="sxs-lookup"><span data-stu-id="2f7f1-107">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="2f7f1-108">次のいずれかのロールに対応する財務にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-108">Access to Finance for one of the following roles:</span></span>
    - <span data-ttu-id="2f7f1-109">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="2f7f1-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="2f7f1-110">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="2f7f1-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="2f7f1-111">システム管理者</span><span class="sxs-lookup"><span data-stu-id="2f7f1-111">System administrator</span></span>

- <span data-ttu-id="2f7f1-112">次のいずれかの役割で、Finance と同じテナントに対してプロビジョニングされている規制コンフィギュレーション サービス (RCS) のインスタンスにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-112">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>
    - <span data-ttu-id="2f7f1-113">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="2f7f1-113">Electronic reporting developer</span></span>
    - <span data-ttu-id="2f7f1-114">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="2f7f1-114">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="2f7f1-115">システム管理者</span><span class="sxs-lookup"><span data-stu-id="2f7f1-115">System administrator</span></span>

<span data-ttu-id="2f7f1-116">このトピックの一部の手順では、ER 形式を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-116">Some steps in this topic require execution of an ER format.</span></span> <span data-ttu-id="2f7f1-117">場合によっては、ER 形式の実行が、現在ログインしている会社の国/地域コンテキストによって影響を受けることがあります。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-117">In some cases, execution of an ER format is affected by the country/region context of the company that you're currently signed in to.</span></span> <span data-ttu-id="2f7f1-118">必要な国/地域コンテキストを RCS で使用できる会社の場合は、現在の RCS インスタンスで ER 形式を実行できます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-118">You can run an ER format in the current RCS instance if the company that has the required country/region context is available in RCS.</span></span> <span data-ttu-id="2f7f1-119">それ以外の場合は、ER データ モデルを使用して ER モデル マッピングと ER 形式コンフィギュレーションの完成版を Finance インスタンスにアップロードし、その Finance インスタンスで ER 形式を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-119">Otherwise, you must upload a completed version of the ER model mapping and ER format configurations that use the ER data model to your Finance instance, and then run the ER format in that Finance instance.</span></span> <span data-ttu-id="2f7f1-120">RCS に格納されているコンフィギュレーションを Finance インスタンスにインポートする方法については、[コンフィギュレーションを RCS からインポートする](rcs-download-configurations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-120">For information about how to import configurations that reside in RCS into a Finance instance, see [Import configurations from RCS](rcs-download-configurations.md).</span></span>

## <a name="single-model-mapping-case"></a><span data-ttu-id="2f7f1-121">単一モデルのマッピング ケース</span><span class="sxs-lookup"><span data-stu-id="2f7f1-121">Single model mapping case</span></span>

<span data-ttu-id="2f7f1-122">このトピックの[付録 1](#appendix1) の手順に従って、必要な ER コンポーネントを設計します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-122">Follow the steps in [Appendix 1](#appendix1) of this topic to design the required ER components.</span></span> <span data-ttu-id="2f7f1-123">これで、**エントリ ポイント 1** 定義のモデル マッピングを含む**マッピング (一般)** モデル マッピング コンフィギュレーションが完成しました。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-123">You now have the **Mapping (General)** model mapping configuration that contains the model mapping for the **Entry point 1** definition.</span></span>

![ER コンフィギュレーション ページ](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="2f7f1-125">構成された形式の実行</span><span class="sxs-lookup"><span data-stu-id="2f7f1-125">Run the configured format</span></span>

1.  <span data-ttu-id="2f7f1-126">**バージョン** クイック タブの**構成ページ**で、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-126">On the **Configurations page**, on the **Versions** FastTab, select **Run**.</span></span>
2.  <span data-ttu-id="2f7f1-127">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-127">Select **OK**.</span></span>

<span data-ttu-id="2f7f1-128">Web ブラウザーで、実行した ER 形式によって生成されたテキスト ファイルをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-128">Notice that the web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="2f7f1-129">この形式は**エントリ ポイント 1** の定義を使用するようにコンフィギュレーションされているため、この定義のマッピングを含む基本モデルで現在使用できるモデル マッピングは 1 つのみです。実行される ER 形式では、**マッピング (一般)** コンフィギュレーションの**マッピング (一般)** モデル マッピングがデータソースとして使用されています。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-129">Because this format was configured to use the **Entry point 1** definition, and only a single model mapping is currently available for the base model that contains a mapping for this definition, the executed ER format used the **Mapping (General)** model mapping of the **Mapping (General)** configuration as a data source.</span></span> <span data-ttu-id="2f7f1-130">このため、ダウンロードしたファイルには、**一般的な機能 1** テキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-130">Therefore, the downloaded file contains the **Generic functionality 1** text.</span></span>

## <a name="multiple-shared-model-mappings-case"></a><span data-ttu-id="2f7f1-131">複数の共有モデルのマッピング ケース</span><span class="sxs-lookup"><span data-stu-id="2f7f1-131">Multiple shared model mappings case</span></span>

<span data-ttu-id="2f7f1-132">このトピックの[付録 2](#appendix2) の手順に従って、必要な ER コンポーネントを設計します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-132">Follow the steps in [Appendix 2](#appendix2) of this topic to design the required ER components.</span></span> <span data-ttu-id="2f7f1-133">これで、それぞれに**エントリ ポイント 1** 定義を含む、**マッピング (一般)** および**マッピング (一般) カスタム** モデル マッピング コンフィギュレーションが完成しました。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-133">You now have **Mapping (General)** and **Mapping (General) custom** model mapping configurations, each of which contains the model mapping for the **Entry point 1** definition.</span></span>

![ER コンフィギュレーション ページ](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="2f7f1-135">構成された形式の実行</span><span class="sxs-lookup"><span data-stu-id="2f7f1-135">Run the configured format</span></span>

1.  <span data-ttu-id="2f7f1-136">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**マッピングを知るための形式**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-136">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="2f7f1-137">**バージョン** クイック タブで、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-137">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="2f7f1-138">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-138">Select **OK**.</span></span>

<span data-ttu-id="2f7f1-139">選択した ER 形式の実行が失敗することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-139">Notice that execution of the selected ER format is unsuccessful.</span></span> <span data-ttu-id="2f7f1-140">**マッピング (一般)** および**マッピング (一般) カスタム** モデル マッピング コンフィギュレーションの、**マッピングを知るためのモデル** モデルおよび**エントリ ポイント 1** 定義に、複数のモデル マッピングが存在することを通知するエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-140">An error message informs you that more than one model mapping exists for the **Model to learn mappings** model and the **Entry point 1** definition in the **Mapping (General)** and **Mapping (General) custom** model mapping configurations.</span></span> <span data-ttu-id="2f7f1-141">また、そのメッセージは、これらのコンフィギュレーションのいずれかを既定のコンフィギュレーションとして選択することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-141">The message also recommends that you select one of those configurations as the default configuration.</span></span>

![ER コンフィギュレーション ページ](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a><span data-ttu-id="2f7f1-143">既定のマッピング コンフィギュレーションの定義</span><span class="sxs-lookup"><span data-stu-id="2f7f1-143">Define a default mapping configuration</span></span>

<span data-ttu-id="2f7f1-144">次の手順に従って、**マッピング (一般) カスタム** モデル マッピング コンフィギュレーションを既定のコンフィギュレーションとして定義します。これにより、そのマッピングを**マッピングを知るための形式** ER 形式のデータ ソースとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-144">Follow these steps to define the **Mapping (General) custom** model mapping configuration as the default configuration, so that its mappings can be used as data sources for the **Format to learn mappings** ER format.</span></span>

1.  <span data-ttu-id="2f7f1-145">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**マッピング (一般) カスタム**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-145">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="2f7f1-146">必要に応じて、**編集**を選択し、現在のページを編集できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-146">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="2f7f1-147">**モデル マッピングの既定値**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-147">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="2f7f1-148">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-148">Select **Save**.</span></span>

![ER コンフィギュレーション ページ](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="2f7f1-150">構成された形式の実行</span><span class="sxs-lookup"><span data-stu-id="2f7f1-150">Run the configured format</span></span>

1.  <span data-ttu-id="2f7f1-151">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**マッピングを知るための形式**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-151">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="2f7f1-152">**バージョン** クイック タブで、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-152">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="2f7f1-153">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-153">Select **OK**.</span></span>

<span data-ttu-id="2f7f1-154">選択した ER 形式の実行が成功することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-154">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="2f7f1-155">Web ブラウザーで、実行した ER 形式によって生成されたテキスト ファイルをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-155">The web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="2f7f1-156">この形式は**エントリ ポイント 1** の定義を使用するようにコンフィギュレーションされているため、**マッピング (一般) カスタム** モデル マッピング コンフィギュレーションが既定のコンフィギュレーションとして選択されます。実行される ER 形式では、**マッピング (一般) カスタム** コンフィギュレーションの**マッピング (一般) コピー** モデル マッピングがデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-156">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="2f7f1-157">このため、ダウンロードしたファイルには、**一般的な機能 1 カスタム** テキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-157">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

> [!NOTE]
> <span data-ttu-id="2f7f1-158">現在ログインしている会社を変更し、この ER 形式を再度実行すると、既定の ER モデル マッピング コンフィギュレーションには会社に依存する制限が含まれないので、生成されたファイルで同じコンテンツを取得できます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-158">If you change the company that you're currently signed in to and run this ER format again, you get the same content in the generated file, because the default ER model mapping configuration doesn't contain any company-dependent restrictions.</span></span>

## <a name="multiple-mixed-model-mappings-case"></a><span data-ttu-id="2f7f1-159">複数の混合モデルのマッピング ケース</span><span class="sxs-lookup"><span data-stu-id="2f7f1-159">Multiple mixed model mappings case</span></span>

<span data-ttu-id="2f7f1-160">このトピックの[付録 3](#appendix3) の手順に従って、必要な ER コンポーネントを設計します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-160">Follow the steps in [Appendix 3](#appendix3) of this topic to design the required ER components.</span></span> <span data-ttu-id="2f7f1-161">これで、**エントリ ポイント 1** 定義のモデル マッピングを含む、**マッピング (一般)**、**マッピング (一般) カスタム**、および**マッピング (FR) モデル マッピング** コンフィギュレーションが完成しました。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-161">You now have **Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR) model mapping** configurations that contain the model mapping for the **Entry point 1** definition.</span></span>

<span data-ttu-id="2f7f1-162">**マッピング (FR)** モデル マッピング コンフィギュレーションのバージョン 1 が、フランスの国/地域のコンテキストがある Finance の会社で実行される、**マッピングを知るためのモデル** モデルの ER 形式にのみ適用されるようにコンフィギュレーションされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-162">Notice that version 1 of the **Mapping (FR)** model mapping configuration is configured so that it applies only to ER formats of the **Model to learn mappings** model that are run in Finance companies that have French country/region context.</span></span>

![ER コンフィギュレーション ページ](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="2f7f1-164">構成された形式の実行</span><span class="sxs-lookup"><span data-stu-id="2f7f1-164">Run the configured format</span></span>

1.  <span data-ttu-id="2f7f1-165">会社を **FRSI** に変更します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-165">Change the company to **FRSI**.</span></span>
2.  <span data-ttu-id="2f7f1-166">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**マッピングを知るための形式**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-166">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
3.  <span data-ttu-id="2f7f1-167">**バージョン** クイック タブで、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-167">On the **Versions** FastTab, select **Run**.</span></span>
4.  <span data-ttu-id="2f7f1-168">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-168">Select **OK**.</span></span>

<span data-ttu-id="2f7f1-169">選択した ER 形式の実行が成功することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-169">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="2f7f1-170">Web ブラウザーで、実行した ER 形式によって生成されたテキスト ファイルをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-170">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="2f7f1-171">この形式は**エントリ ポイント 1** の定義を使用するようにコンフィギュレーションされているため、**マッピング (一般) カスタム** モデル マッピング コンフィギュレーションが既定のコンフィギュレーションとして選択されます。実行される ER 形式では、**マッピング (一般) カスタム** コンフィギュレーションの**マッピング (一般) コピー** モデル マッピングがデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-171">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="2f7f1-172">このため、ダウンロードしたファイルには、**一般的な機能 1 カスタム** テキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-172">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a><span data-ttu-id="2f7f1-173">既定のコンフィギュレーションとしての、フランス固有のマッピング コンフィギュレーションの定義</span><span class="sxs-lookup"><span data-stu-id="2f7f1-173">Define the France-specific mapping configuration as the default configuration</span></span>

<span data-ttu-id="2f7f1-174">次の手順に従って、既定のコンフィギュレーションとして、カスタム **マッピング (FR)** モデル マッピング コンフィギュレーションを定義します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-174">Follow these steps to define the custom **Mapping (FR)** model mapping configuration as the default configuration.</span></span> <span data-ttu-id="2f7f1-175">このマッピングはフランスに固有であるため、**ISO 国 / 地域コード** フィールドで、**FR** の国コードが指定されているすべてのモデル マッピング コンフィギュレーションの既定のマッピングが考慮されます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-175">Note that, because this mapping is specific to France, it will be considered the default mapping between all model mapping configurations that have the **FR** country code specified in the **ISO country/region codes** field.</span></span>

1.  <span data-ttu-id="2f7f1-176">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**マッピング (FR)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-176">On the **Configurations** page, in the configurations tree, select **Mapping (FR)**.</span></span>
2.  <span data-ttu-id="2f7f1-177">必要に応じて、**編集**を選択し、現在のページを編集できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-177">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="2f7f1-178">**モデル マッピングの既定値**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-178">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="2f7f1-179">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-179">Select **Save**.</span></span>

![ER コンフィギュレーション ページ](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="2f7f1-181">構成された形式の実行</span><span class="sxs-lookup"><span data-stu-id="2f7f1-181">Run the configured format</span></span>

1.  <span data-ttu-id="2f7f1-182">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**マッピングを知るための形式**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-182">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="2f7f1-183">**バージョン** クイック タブで、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-183">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="2f7f1-184">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-184">Select **OK**.</span></span>

<span data-ttu-id="2f7f1-185">選択した ER 形式の実行が成功することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-185">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="2f7f1-186">Web ブラウザーで、実行した ER 形式によって生成されたテキスト ファイルをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-186">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="2f7f1-187">この形式は**エントリ ポイント 1** の定義を使用するようにコンフィギュレーションされているため、**マッピング (FR)** モデル マッピング コンフィギュレーションが既定のコンフィギュレーションとして選択されます。実行される ER 形式では、**マッピング (FR)** コンフィギュレーションの**マッピング (FR) コピー** モデル マッピングがデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-187">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (FR)** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (FR)** model mapping of the **Mapping (FR)** configuration as a data source.</span></span> <span data-ttu-id="2f7f1-188">このため、ダウンロードしたファイルには、**FR 機能 1** テキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-188">Therefore, the downloaded file contains the **FR functionality 1** text.</span></span>

> [!NOTE]
> <span data-ttu-id="2f7f1-189">現在ログインしている会社を変更し、この ER 形式を再度実行した場合、出力は、選択した会社の国/地域のコンテキストによって異なります。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-189">If you change the company that you're currently signed in to and run this ER format again, the output will depend on the country/region context of the selected company.</span></span>

## <a name="other-model-mapping-cases"></a><span data-ttu-id="2f7f1-190">他のモデルのマッピング ケース</span><span class="sxs-lookup"><span data-stu-id="2f7f1-190">Other model mapping cases</span></span>

<span data-ttu-id="2f7f1-191">既に説明したように、ER 形式を実行するためのモデル マッピングの選択は、次のように機能します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-191">As you've seen, the selection of a model mapping for the execution of an ER format works in the following way:</span></span>

- <span data-ttu-id="2f7f1-192">ER 形式によって使用されるモデル マッピング定義 (このトピックの例では**エントリ ポイント 1**) を指定します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-192">The model mapping definition that an ER format uses is specified (**Entry point 1** in the examples in this topic).</span></span>
- <span data-ttu-id="2f7f1-193">指定された定義のあるマッピングと、コンフィギュレーションされた国/地域のコンテキスト制限を満たすマッピング コンフィギュレーションのすべてが、ER 形式を実行するために使用される可能性があります (このトピックの例では、**マッピング (一般)**、**マッピング (一般) カスタム**、および**マッピング (FR)**)。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-193">All mapping configurations that contain a mapping that has the specified definition, and that satisfy any country/region context restrictions that are configured, can potentially be used to run the ER format (**Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="2f7f1-194">国/地域コンテキストの制限のある既定のモデル マッピングは、選択の優先順位が最も高くなります (このトピックの例では**マッピング (FR)**)。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-194">Any default model mapping that has country/region context restrictions has the highest priority for selection (**Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="2f7f1-195">国/地域コンテキストの制限のない既定のモデル マッピングは、選択の優先順位が次に高くなります (このトピックの例では**マッピング (一般) カスタム**)。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-195">Any default model mapping that doesn't have country/region context restrictions has the next higher priority for selection  (**Mapping (General) custom** in the examples in this topic).</span></span>
- <span data-ttu-id="2f7f1-196">国/地域コンテキストの制限があるモデル マッピングは、国/地域コンテキストの制限のないモデル マッピングよりも選択の優先順位が高くなります。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-196">Any model mapping that has country/region context restrictions has higher priority for selection than a model mapping that doesn't have country/region context restrictions.</span></span>

<span data-ttu-id="2f7f1-197">次の表に、モデル マッピング設定が可能なすべてのケースの、モデル マッピング選択の結果についての情報を示します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-197">The following table provides information about the results of model mapping selection for all possible cases for model mapping settings:</span></span>

- <span data-ttu-id="2f7f1-198">列 1 は、国/地域コンテキストの制限のない最初のモデル マッピング (共有**マッピング (一般)** マッピングなど) が存在するかどうかを示し、存在する場合、**モデル マッピングの既定値**オプションが**はい**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-198">Column 1 indicates whether the first model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="2f7f1-199">列 2 は、国/地域コンテキストの制限のない 2 番目のモデル マッピング (共有**マッピング (一般) カスタム** マッピングなど) が存在するかどうかを示し、存在する場合、**モデル マッピングの既定値**オプションが**はい**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-199">Column 2 indicates whether the second model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General) custom** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="2f7f1-200">列 3 は、国/地域 A のコンテキストの制限のある最初のモデル マッピング (フランス固有の**マッピング (FR)** マッピングなど) が存在するかどうかを示し、存在する場合、**モデル マッピングの既定値**オプションが**はい**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-200">Column 3 indicates whether the first model mapping that has country/region A context restrictions (for example, the France-specific **Mapping (FR)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="2f7f1-201">列 4 は、国/地域 A のコンテキストの制限のある 2 番目のモデル マッピングが存在するかどうかを示し、存在する場合、**モデル マッピングの既定値**オプションが**はい**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-201">Column 4 indicates whether the second model mapping that has country/region A context restrictions is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="2f7f1-202">列 5 は、国/地域 A のコンテキストのある会社の管理下で ER 形式を実行するためのモデル マッピング選択の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-202">Column 5 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region A context.</span></span>
- <span data-ttu-id="2f7f1-203">列 6 は、国/地域 B のコンテキストのある会社の管理下で ER 形式を実行するためのモデル マッピング選択の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-203">Column 6 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region B context.</span></span>

<span data-ttu-id="2f7f1-204">この表では、プラス記号 (+) はER 形式 (Finance または RCS) を実行するために使用される Microsoft Azure サービスの現在のインスタンスにモデル マッピング コンフィギュレーションが存在することを示します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-204">In the table, a plus sign (+) indicates the presence of a model mapping configuration in the current instance of the Microsoft Azure service that is used to run an ER format (either Finance or RCS).</span></span>

| <span data-ttu-id="2f7f1-205">ケース</span><span class="sxs-lookup"><span data-stu-id="2f7f1-205">Case</span></span> | <span data-ttu-id="2f7f1-206">国/地域コンテキストがないモデル マッピング 1 (MM1)</span><span class="sxs-lookup"><span data-stu-id="2f7f1-206">Model mapping 1 without country/region context (MM1)</span></span> | <span data-ttu-id="2f7f1-207">国/地域コンテキストがないモデル マッピング 2 (MM2)</span><span class="sxs-lookup"><span data-stu-id="2f7f1-207">Model mapping 2 without country/region context (MM2)</span></span> | <span data-ttu-id="2f7f1-208">国/地域 A のコンテキストがあるモデル マッピング 1 (MM1A)</span><span class="sxs-lookup"><span data-stu-id="2f7f1-208">Model mapping 1 with country/region A context (MM1A)</span></span> | <span data-ttu-id="2f7f1-209">国/地域 A のコンテキストがあるモデル マッピング 2 (MM2A)</span><span class="sxs-lookup"><span data-stu-id="2f7f1-209">Model mapping 2 with country/region A context (MM2A)</span></span> | <span data-ttu-id="2f7f1-210">国/地域 A コンテキストのある会社の管理下で実行する</span><span class="sxs-lookup"><span data-stu-id="2f7f1-210">Run under control of a company that has country/region A context</span></span> | <span data-ttu-id="2f7f1-211">国/地域 B コンテキストのある会社の管理下で実行する</span><span class="sxs-lookup"><span data-stu-id="2f7f1-211">Run under the control of a company that has country/region B context</span></span> |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     <span data-ttu-id="2f7f1-212">1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-212">1</span></span>   |     <span data-ttu-id="2f7f1-213">2</span><span class="sxs-lookup"><span data-stu-id="2f7f1-213">2</span></span>   |    <span data-ttu-id="2f7f1-214">3</span><span class="sxs-lookup"><span data-stu-id="2f7f1-214">3</span></span>    |    <span data-ttu-id="2f7f1-215">4</span><span class="sxs-lookup"><span data-stu-id="2f7f1-215">4</span></span>    |           <span data-ttu-id="2f7f1-216">5</span><span class="sxs-lookup"><span data-stu-id="2f7f1-216">5</span></span>               |            <span data-ttu-id="2f7f1-217">6</span><span class="sxs-lookup"><span data-stu-id="2f7f1-217">6</span></span>               |
|     <span data-ttu-id="2f7f1-218">1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-218">1</span></span>   |         |         |         |         | <span data-ttu-id="2f7f1-219">エラー (マッピングがありません)</span><span class="sxs-lookup"><span data-stu-id="2f7f1-219">Error (missing mapping)</span></span>   | <span data-ttu-id="2f7f1-220">エラー (マッピングがありません)</span><span class="sxs-lookup"><span data-stu-id="2f7f1-220">Error (missing mapping)</span></span>    |
|     <span data-ttu-id="2f7f1-221">2</span><span class="sxs-lookup"><span data-stu-id="2f7f1-221">2</span></span>   |     +   |         |         |         | <span data-ttu-id="2f7f1-222">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-222">MM1</span></span>                       | <span data-ttu-id="2f7f1-223">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-223">MM1</span></span>                        |
|     <span data-ttu-id="2f7f1-224">3</span><span class="sxs-lookup"><span data-stu-id="2f7f1-224">3</span></span>   |     +   |     +   |         |         | <span data-ttu-id="2f7f1-225">エラー (複数のマッピング)</span><span class="sxs-lookup"><span data-stu-id="2f7f1-225">Error (multiple mappings)</span></span> | <span data-ttu-id="2f7f1-226">エラー (複数のマッピング)</span><span class="sxs-lookup"><span data-stu-id="2f7f1-226">Error (multiple mappings)</span></span>  |
|     <span data-ttu-id="2f7f1-227">4</span><span class="sxs-lookup"><span data-stu-id="2f7f1-227">4</span></span>   |     +   |         |    +    |         | <span data-ttu-id="2f7f1-228">MM1A</span><span class="sxs-lookup"><span data-stu-id="2f7f1-228">MM1A</span></span>                      | <span data-ttu-id="2f7f1-229">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-229">MM1</span></span>                        |
|     <span data-ttu-id="2f7f1-230">5</span><span class="sxs-lookup"><span data-stu-id="2f7f1-230">5</span></span>   |     +   |         |    +    |    +    | <span data-ttu-id="2f7f1-231">エラー (複数のマッピング)</span><span class="sxs-lookup"><span data-stu-id="2f7f1-231">Error (multiple mappings)</span></span> | <span data-ttu-id="2f7f1-232">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-232">MM1</span></span>                        |
|     <span data-ttu-id="2f7f1-233">6</span><span class="sxs-lookup"><span data-stu-id="2f7f1-233">6</span></span>   |     +   | <span data-ttu-id="2f7f1-234">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-234">default</span></span> |    +    |    +    | <span data-ttu-id="2f7f1-235">MM2</span><span class="sxs-lookup"><span data-stu-id="2f7f1-235">MM2</span></span>                       | <span data-ttu-id="2f7f1-236">MM2</span><span class="sxs-lookup"><span data-stu-id="2f7f1-236">MM2</span></span>                        |
|     <span data-ttu-id="2f7f1-237">7</span><span class="sxs-lookup"><span data-stu-id="2f7f1-237">7</span></span>   |     +   |         | <span data-ttu-id="2f7f1-238">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-238">default</span></span> |         | <span data-ttu-id="2f7f1-239">MM1A</span><span class="sxs-lookup"><span data-stu-id="2f7f1-239">MM1A</span></span>                      | <span data-ttu-id="2f7f1-240">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-240">MM1</span></span>                        |
|     <span data-ttu-id="2f7f1-241">8</span><span class="sxs-lookup"><span data-stu-id="2f7f1-241">8</span></span>   |     +   |         | <span data-ttu-id="2f7f1-242">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-242">default</span></span> |    +    | <span data-ttu-id="2f7f1-243">MM1A</span><span class="sxs-lookup"><span data-stu-id="2f7f1-243">MM1A</span></span>                      | <span data-ttu-id="2f7f1-244">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-244">MM1</span></span>                        |
|     <span data-ttu-id="2f7f1-245">9</span><span class="sxs-lookup"><span data-stu-id="2f7f1-245">9</span></span>   |     +   |         | <span data-ttu-id="2f7f1-246">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-246">default</span></span> | <span data-ttu-id="2f7f1-247">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-247">default</span></span> | <span data-ttu-id="2f7f1-248">エラー (複数のマッピング)</span><span class="sxs-lookup"><span data-stu-id="2f7f1-248">Error (multiple mappings)</span></span> | <span data-ttu-id="2f7f1-249">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-249">MM1</span></span>                        |
|    <span data-ttu-id="2f7f1-250">10</span><span class="sxs-lookup"><span data-stu-id="2f7f1-250">10</span></span>   | <span data-ttu-id="2f7f1-251">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-251">default</span></span> |         |         |         | <span data-ttu-id="2f7f1-252">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-252">MM1</span></span>                       | <span data-ttu-id="2f7f1-253">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-253">MM1</span></span>                        |
|    <span data-ttu-id="2f7f1-254">11</span><span class="sxs-lookup"><span data-stu-id="2f7f1-254">11</span></span>   | <span data-ttu-id="2f7f1-255">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-255">default</span></span> |    +    |         |         | <span data-ttu-id="2f7f1-256">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-256">MM1</span></span>                       | <span data-ttu-id="2f7f1-257">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-257">MM1</span></span>                        |
|    <span data-ttu-id="2f7f1-258">12</span><span class="sxs-lookup"><span data-stu-id="2f7f1-258">12</span></span>   | <span data-ttu-id="2f7f1-259">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-259">default</span></span> |         |    +    |         | <span data-ttu-id="2f7f1-260">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-260">MM1</span></span>                       | <span data-ttu-id="2f7f1-261">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-261">MM1</span></span>                        |
|    <span data-ttu-id="2f7f1-262">13</span><span class="sxs-lookup"><span data-stu-id="2f7f1-262">13</span></span>   | <span data-ttu-id="2f7f1-263">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-263">default</span></span> | <span data-ttu-id="2f7f1-264">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-264">default</span></span> |         |         | <span data-ttu-id="2f7f1-265">エラー (複数のマッピング)</span><span class="sxs-lookup"><span data-stu-id="2f7f1-265">Error (multiple mappings)</span></span> | <span data-ttu-id="2f7f1-266">エラー (複数のマッピング)</span><span class="sxs-lookup"><span data-stu-id="2f7f1-266">Error (multiple mappings)</span></span>  |
|    <span data-ttu-id="2f7f1-267">14</span><span class="sxs-lookup"><span data-stu-id="2f7f1-267">14</span></span>   | <span data-ttu-id="2f7f1-268">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-268">default</span></span> |         | <span data-ttu-id="2f7f1-269">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-269">default</span></span> |         | <span data-ttu-id="2f7f1-270">MM1A</span><span class="sxs-lookup"><span data-stu-id="2f7f1-270">MM1A</span></span>                      | <span data-ttu-id="2f7f1-271">MM1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-271">MM1</span></span>                        |
|    <span data-ttu-id="2f7f1-272">15</span><span class="sxs-lookup"><span data-stu-id="2f7f1-272">15</span></span>   | <span data-ttu-id="2f7f1-273">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-273">default</span></span> |         | <span data-ttu-id="2f7f1-274">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-274">default</span></span> | <span data-ttu-id="2f7f1-275">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-275">default</span></span> | <span data-ttu-id="2f7f1-276">MM1A</span><span class="sxs-lookup"><span data-stu-id="2f7f1-276">MM1A</span></span>                      | <span data-ttu-id="2f7f1-277">MM2A</span><span class="sxs-lookup"><span data-stu-id="2f7f1-277">MM2A</span></span>                       |
|    <span data-ttu-id="2f7f1-278">16</span><span class="sxs-lookup"><span data-stu-id="2f7f1-278">16</span></span>   |         |         |    +    |    +    | <span data-ttu-id="2f7f1-279">MM1A</span><span class="sxs-lookup"><span data-stu-id="2f7f1-279">MM1A</span></span>                      | <span data-ttu-id="2f7f1-280">MM2A</span><span class="sxs-lookup"><span data-stu-id="2f7f1-280">MM2A</span></span>                       |
|    <span data-ttu-id="2f7f1-281">17</span><span class="sxs-lookup"><span data-stu-id="2f7f1-281">17</span></span>   |         |         | <span data-ttu-id="2f7f1-282">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-282">default</span></span> | <span data-ttu-id="2f7f1-283">既定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-283">default</span></span> | <span data-ttu-id="2f7f1-284">MM1A</span><span class="sxs-lookup"><span data-stu-id="2f7f1-284">MM1A</span></span>                      | <span data-ttu-id="2f7f1-285">MM2A</span><span class="sxs-lookup"><span data-stu-id="2f7f1-285">MM2A</span></span>                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a><span data-ttu-id="2f7f1-286">ER 形式の実行に使用されたマッピングについて</span><span class="sxs-lookup"><span data-stu-id="2f7f1-286">Learn what mapping was used in the execution of an ER format</span></span>

### <a name="configure-er-user-parameters"></a><span data-ttu-id="2f7f1-287">ER ユーザー パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2f7f1-287">Configure ER user parameters</span></span>

1.  <span data-ttu-id="2f7f1-288">**構成**ページのアクション ウィンドウの**コンフィギュレーション** タブで、**ユーザー パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-288">On the **Configurations** page, on the Action Pane, on the **CONFIGURATIONS** tab, select **User parameters**.</span></span>
2.  <span data-ttu-id="2f7f1-289">**デバッグモードで実行する**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-289">Set the **Run in debug mode** option to **Yes**.</span></span>
4.  <span data-ttu-id="2f7f1-290">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-290">Select **Ok**.</span></span>

### <a name="run-the-configured-format"></a><span data-ttu-id="2f7f1-291">構成された形式の実行</span><span class="sxs-lookup"><span data-stu-id="2f7f1-291">Run the configured format</span></span>

1.  <span data-ttu-id="2f7f1-292">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**マッピングを知るための形式**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-292">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="2f7f1-293">**バージョン** クイック タブで、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-293">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="2f7f1-294">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-294">Select **Ok**.</span></span>

### <a name="review-the-er-debug-log"></a><span data-ttu-id="2f7f1-295">ER デバッグ ログを確認する</span><span class="sxs-lookup"><span data-stu-id="2f7f1-295">Review the ER debug log</span></span>

1.  <span data-ttu-id="2f7f1-296">ナビゲーション ウィンドウで、**モジュール \> 組織の管理 \> 電子申告 \> 構成デバッグ ログ**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-296">In the navigation pane, go to **Modules \> Organization administration \> Electronic reporting \> Configuration debug log**.</span></span>
2.  <span data-ttu-id="2f7f1-297">**このページを再読み込みする**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-297">Select the **Reload this page** button.</span></span>

![ER 実行ログ ページ](./media/RCS-Context-specific-mapping-DebugLog.PNG)

<span data-ttu-id="2f7f1-299">実行される ER 形式の ER デバッグ ログに新しいレコードが追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-299">Notice that a new record has been added to the ER debug log for the executed ER format.</span></span> <span data-ttu-id="2f7f1-300">このレコードの**レベル**フィールドは**情報**に設定されているので、レコードは情報になります。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-300">Because the **Level** field of this record is set to **Info**, the record is informational.</span></span> <span data-ttu-id="2f7f1-301">形式コンポーネント フィールドは、**マッピング コンフィギュレーション**に設定されているので、(**コンフィギュレーション名** フィールドで選択された) **マッピングを知るための形式** ER 形式 の実行中に使用されたモデル マッピングについての通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-301">Because the Format component field is set to **Mapping configuration**, the record informs you about a model mapping that was used during execution of the **Format to learn mappings** ER format (selected in the **Configuration name** field).</span></span> <span data-ttu-id="2f7f1-302">**生成されたテキスト** フィールドの内容は、**マッピング (FR)** コンフィグレーションの **マッピング (FR)** が、このレポートの実行に使用されたことを通知します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-302">The content of the **Generated text** field informs you that the **Mapping (FR)** mapping component that resides in the **Mapping (FR)** configuration has been used to run this report.</span></span>

## <a name="appendix1"></a><span data-ttu-id="2f7f1-303">付録 1</span><span class="sxs-lookup"><span data-stu-id="2f7f1-303">Appendix 1</span></span>

### <a name="configure-a-sample-data-model"></a><span data-ttu-id="2f7f1-304">サンプル データ モデルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2f7f1-304">Configure a sample data model</span></span>

<span data-ttu-id="2f7f1-305">RCS インスタンスにサインインする。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-305">Sign in to your RCS instance.</span></span>

<span data-ttu-id="2f7f1-306">この例では、サンプル会社 Litware, Inc. 用に、コンフィギュレーションを作成します。これらの手順を完了するには、まず、RCS で、手順 [コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md) にあるステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-306">In this example, you will create a configuration for sample company, Litware, Inc. To complete these steps, you must first complete, in RCS, the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

#### <a name="create-an-er-data-model-configuration"></a><span data-ttu-id="2f7f1-307">ER データ モデル コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="2f7f1-307">Create an ER data model configuration</span></span>

1.  <span data-ttu-id="2f7f1-308">既定のダッシュボードで、**電子申告**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-308">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="2f7f1-309">**コンフィギュレーションをレポートする**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-309">Select the **Reporting configurations** tile.</span></span>
3.  <span data-ttu-id="2f7f1-310">**コンフィギュレーション**ページで、**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-310">On the **Configurations** page, select **Create configuration**.</span></span>
4.  <span data-ttu-id="2f7f1-311">**名前**フィールドのドロップダウン ダイアログ ボックスに、**マッピングを知るためのモデル**を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-311">In the drop-down dialog box, in the **Name** field, enter **Model to learn mappings**.</span></span>
5.  <span data-ttu-id="2f7f1-312">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-312">Select **Create configuration**.</span></span>
6.  <span data-ttu-id="2f7f1-313">**コンポーネントのコンフィギュレーション** クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-313">Select the **Configuration components** FastTab.</span></span>

<span data-ttu-id="2f7f1-314">この ER コンフィギュレーションのドラフト バージョン 1 を編集する準備ができていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-314">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="2f7f1-315">このバージョンには、データ モデル コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-315">This version contains the data model component.</span></span>

#### <a name="design-a-sample-data-model"></a><span data-ttu-id="2f7f1-316">サンプル データ モデルのデザイン</span><span class="sxs-lookup"><span data-stu-id="2f7f1-316">Design a sample data model</span></span>

1.  <span data-ttu-id="2f7f1-317">**コンフィギュレーション**ページで、**デザイナー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-317">On the **Configurations page**, select **Designer**.</span></span>
2.  <span data-ttu-id="2f7f1-318">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-318">Select **New**.</span></span>
3.  <span data-ttu-id="2f7f1-319">ドロップダウン ダイアログボックスの**名前**フィールドに**エントリ ポイント 1** を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-319">In the drop-down dialog box, in the **Name** field, enter **Entry point 1**.</span></span>
4.  <span data-ttu-id="2f7f1-320">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-320">Select **Add**.</span></span>
5.  <span data-ttu-id="2f7f1-321">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-321">Select **New**.</span></span>
6.  <span data-ttu-id="2f7f1-322">**名前**フィールドのドロップダウン ダイアログ ボックスに、**機能説明**を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-322">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
7.  <span data-ttu-id="2f7f1-323">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-323">Select **Add**.</span></span>
8.  <span data-ttu-id="2f7f1-324">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-324">Select **New**.</span></span>
9.  <span data-ttu-id="2f7f1-325">**新しいノード**フィールド グループのドロップダウン ダイアログ ボックスで、**モデル ルート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-325">In the drop-down dialog box, in the **New node** field group, select **Model root**.</span></span>
10. <span data-ttu-id="2f7f1-326">**名前**フィールドに、**エントリ ポイント 2** を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-326">In the **Name** field, enter **Entry point 2**.</span></span>
11. <span data-ttu-id="2f7f1-327">**エントリ ポイント 2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-327">Select **Entry point 2**.</span></span>
12. <span data-ttu-id="2f7f1-328">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-328">Select **Add**.</span></span>
13. <span data-ttu-id="2f7f1-329">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-329">Select **New**.</span></span>
14. <span data-ttu-id="2f7f1-330">**名前**フィールドのドロップダウン ダイアログ ボックスに、**機能説明**を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-330">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
15. <span data-ttu-id="2f7f1-331">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-331">Select **Add**.</span></span>

    ![ER データ モデル デザイナーのページ](./media/RCS-Context-specific-mapping-Model.PNG)

16. <span data-ttu-id="2f7f1-333">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-333">Select **Save**.</span></span>
17. <span data-ttu-id="2f7f1-334">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-334">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-configuration"></a><span data-ttu-id="2f7f1-335">モデル コンフィギュレーションの変更されたバージョンを完了する</span><span class="sxs-lookup"><span data-stu-id="2f7f1-335">Complete the modified version of the model configuration</span></span>

1.  <span data-ttu-id="2f7f1-336">**バージョン** クイック タブの**コンフィギュレーション** ページで、**ステータスの変更**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-336">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="2f7f1-337">設計されたモデル コンフィギュレーションのステータスを**ドラフト**から**完了**に変更し、必要なモデル マッピングと形式を設計するために使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-337">Change the status of designed model configuration from **Draft** to **Completed**, so that it can be used to design the required model mappings and formats.</span></span>

2.  <span data-ttu-id="2f7f1-338">**完了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-338">Select **Complete**.</span></span>
3.  <span data-ttu-id="2f7f1-339">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-339">Select **OK**.</span></span>

<span data-ttu-id="2f7f1-340">作成したコンフィギュレーションが完了したバージョン 1 として保存されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-340">Notice that the configuration that you created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-model-mapping"></a><span data-ttu-id="2f7f1-341">サンプル モデル マッピングのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2f7f1-341">Configure a sample model mapping</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="2f7f1-342">ER モデル マッピング コンフィギュレーションを作成する</span><span class="sxs-lookup"><span data-stu-id="2f7f1-342">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="2f7f1-343">**コンフィギュレーション**ページで、**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-343">On the **Configurations** page, select **Create configuration**.</span></span>
2.  <span data-ttu-id="2f7f1-344">ドロップダウン ダイアログ ボックスにある**新しい**フィールド グループで、**マッピングを知るためのモデル データ モデルに基づくモデル マッピング**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-344">In the drop-down dialog box, in the **New** field group, select **Model mapping based on data model Model to learn mappings**.</span></span>
3.  <span data-ttu-id="2f7f1-345">**名前**フィールドに、**マッピング (一般)** を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-345">In the **Name** field, enter **Mapping (General)**.</span></span>
4.  <span data-ttu-id="2f7f1-346">**データ モデル定義**フィールドで、**エントリ ポイント 1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-346">In the **Data model definition** field, select **Entry point 1**.</span></span>
5.  <span data-ttu-id="2f7f1-347">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-347">Select **Create configuration**.</span></span>

<span data-ttu-id="2f7f1-348">この ER コンフィギュレーションのドラフト バージョン 1 を編集する準備ができていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-348">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="2f7f1-349">このバージョンには、モデル マッピング コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-349">This version contains the model mapping component.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="2f7f1-350">サンプル モデル マッピングのデザイン</span><span class="sxs-lookup"><span data-stu-id="2f7f1-350">Design a sample model mapping</span></span>

1.  <span data-ttu-id="2f7f1-351">**構成**ページで、**デザイナー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-351">On the **Configurations** page, select **Designer**.</span></span>

    <span data-ttu-id="2f7f1-352">**モデルへ**方向タイプのモデル マッピングが、**エントリポイント 1** 定義の、このコンポーネントに自動的に追加されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-352">Notice that the model mapping of the **To model** direction type has been automatically added to this component for the **Entry point 1** definition.</span></span>
    
2.  <span data-ttu-id="2f7f1-353">追加したモデル マッピングの編集を開始するには、**デザイナー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-353">Select **Designer** to start editing the added model mapping.</span></span>
3.  <span data-ttu-id="2f7f1-354">**データ モデル** セクションで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-354">In the **Data model** section, select **Edit**.</span></span>
4.  <span data-ttu-id="2f7f1-355">**式**フィールドに、**一般的な機能 1** を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-355">In the **Formula** field, enter **"Generic functionality 1"**.</span></span>
5.  <span data-ttu-id="2f7f1-356">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-356">Select **Save**.</span></span>
6.  <span data-ttu-id="2f7f1-357">**フォーミュラ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-357">Close the **Formula designer** page.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  <span data-ttu-id="2f7f1-359">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-359">Select **Save**.</span></span>
8.  <span data-ttu-id="2f7f1-360">**モデル マッピング デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-360">Close the **Model mapping designer** page.</span></span>
9.  <span data-ttu-id="2f7f1-361">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-361">Select **New**.</span></span>
10. <span data-ttu-id="2f7f1-362">**定義**フィールドで、**エントリ ポイント 2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-362">In the **Definition** field, select **Entry point 2**.</span></span>
11. <span data-ttu-id="2f7f1-363">**名前**フィールドに、**マッピング (一般) 2** を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-363">In the **Name** field, enter **Mapping (General) 2**.</span></span>
12. <span data-ttu-id="2f7f1-364">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-364">Select **Designer**.</span></span>
13. <span data-ttu-id="2f7f1-365">**データ モデル** セクションで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-365">In the **Data model** section, select **Edit**.</span></span>
14. <span data-ttu-id="2f7f1-366">**式**フィールドに、**一般的な機能 2** を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-366">In the **Formula** field, enter **"Generic functionality 2"**.</span></span>
15. <span data-ttu-id="2f7f1-367">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-367">Select **Save**.</span></span>
16. <span data-ttu-id="2f7f1-368">**フォーミュラ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-368">Close the **Formula designer** page.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. <span data-ttu-id="2f7f1-370">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-370">Select **Save**.</span></span>
18. <span data-ttu-id="2f7f1-371">**モデル マッピング デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-371">Close the **Model mapping designer** page.</span></span>

    ![ER モデル マッピング ページ](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. <span data-ttu-id="2f7f1-373">**モデル マッピング** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-373">Close the **Model mappings** page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="2f7f1-374">モデル マッピング コンフィギュレーションの変更されたバージョンを完了する</span><span class="sxs-lookup"><span data-stu-id="2f7f1-374">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="2f7f1-375">**バージョン** クイック タブの**コンフィギュレーション** ページで、**ステータスの変更**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-375">On the **Configurations page**, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="2f7f1-376">設計されたモデル マッピング コンフィギュレーションのステータスを**ドラフト**から**完了**に変更し、ER 形式で使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-376">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="2f7f1-377">**完了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-377">Select **Complete**.</span></span>
3.  <span data-ttu-id="2f7f1-378">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-378">Select **OK**.</span></span>

<span data-ttu-id="2f7f1-379">作成したコンフィギュレーションが完了したバージョン 1 として保存されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-379">Notice that the configuration that is created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-format"></a><span data-ttu-id="2f7f1-380">サンプル形式のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2f7f1-380">Configure a sample format</span></span>

#### <a name="create-an-er-format-configuration"></a><span data-ttu-id="2f7f1-381">ER 形式コンフィギュレーションを作成する</span><span class="sxs-lookup"><span data-stu-id="2f7f1-381">Create an ER format configuration</span></span>

1.  <span data-ttu-id="2f7f1-382">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**マッピングを知るためのモデル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-382">On the **Configurations** page, in the configurations tree, select **Model to learn mappings**.</span></span>
2.  <span data-ttu-id="2f7f1-383">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-383">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="2f7f1-384">ドロップダウン ダイアログ ボックスにある**新しい**フィールド グループで、**マッピングを知るためのモデル データ モデルに基づく形式**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-384">In the drop-down dialog box, in the **New** field group, select **Format based on data model Model to learn mappings**.</span></span>
4.  <span data-ttu-id="2f7f1-385">**名前**フィールドに、**マッピングを知るための形式**を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-385">In the **Name** field, enter **Format to learn mappings**.</span></span>
5.  <span data-ttu-id="2f7f1-386">**データ モデル定義**フィールドで、**エントリ ポイント 1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-386">In the **Data model definition** field, select **Entry point 1**.</span></span>
6.  <span data-ttu-id="2f7f1-387">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-387">Select **Create configuration**.</span></span>

<span data-ttu-id="2f7f1-388">この ER コンフィギュレーションのドラフト バージョン 1 を編集する準備ができていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-388">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="2f7f1-389">このバージョンには、形式コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-389">This version contains the format component.</span></span>

#### <a name="design-a-sample-format"></a><span data-ttu-id="2f7f1-390">サンプル形式のデザイン</span><span class="sxs-lookup"><span data-stu-id="2f7f1-390">Design a sample format</span></span>

1.  <span data-ttu-id="2f7f1-391">**構成**ページで、**デザイナー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-391">On the **Configurations** page, select **Designer**.</span></span>
2.  <span data-ttu-id="2f7f1-392">**ルートの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-392">Select **Add root**.</span></span>
3.  <span data-ttu-id="2f7f1-393">**テキスト** グループで、**文字列**項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-393">In the **Text** group, select the **String** item.</span></span>
4.  <span data-ttu-id="2f7f1-394">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-394">Select **OK**.</span></span>

#### <a name="bind-format-elements-to-a-data-source"></a><span data-ttu-id="2f7f1-395">形式要素をデータソースにバインドする</span><span class="sxs-lookup"><span data-stu-id="2f7f1-395">Bind format elements to a data source</span></span>

1.  <span data-ttu-id="2f7f1-396">**形式デザイナー** ページの**マッピング** タブで、モデル データソースを展開します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-396">On the **Format designer** page, on the **Mapping** tab, expand the model data source.</span></span>
2.  <span data-ttu-id="2f7f1-397">**機能説明**フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-397">Select the **Functionality description** field.</span></span>
3.  <span data-ttu-id="2f7f1-398">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-398">Select **Bind**.</span></span>

    ![ER 形式デザイナーのページ](./media/RCS-Context-specific-mapping-Format.PNG)

4.  <span data-ttu-id="2f7f1-400">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-400">Select **Save**.</span></span>
5.  <span data-ttu-id="2f7f1-401">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-401">Close the page.</span></span>

## <a name="appendix2"></a><span data-ttu-id="2f7f1-402">付録 2</span><span class="sxs-lookup"><span data-stu-id="2f7f1-402">Appendix 2</span></span>

### <a name="configure-a-sample-model-mapping-for-general-customization"></a><span data-ttu-id="2f7f1-403">一般的なカスタマイズのために、サンプル モデル マッピングをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="2f7f1-403">Configure a sample model mapping for general customization</span></span>

<span data-ttu-id="2f7f1-404">必要に応じて、コンフィギュレーション プロバイダー (パートナー) から提供されたモデル マッピングをカスタマイズし、カスタマイズされたバージョンを ER 形式のデータソースとして使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-404">You might want to customize a model mapping that a configuration provider (partner) provided to you, and then use the customized version as a data source for your ER formats.</span></span> <span data-ttu-id="2f7f1-405">この場合、既存のモデル マッピングに必要な変更を加えるには、カスタム ER モデル マッピング コンフィギュレーションを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-405">In this case, you must create a custom ER model mapping configuration to make the required changes in existing model mappings.</span></span> <span data-ttu-id="2f7f1-406">この付録の手順では、**マッピング (一般)** モデル マッピングを例として使用します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-406">The procedures in this appendix use the **Mapping (General)** model mapping as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="2f7f1-407">ER モデル マッピング コンフィギュレーションを作成する</span><span class="sxs-lookup"><span data-stu-id="2f7f1-407">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="2f7f1-408">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**マッピング (一般)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-408">On the **Configurations** page, in the configurations tree, select **Mapping (General)**.</span></span>
2.  <span data-ttu-id="2f7f1-409">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-409">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="2f7f1-410">ドロップダウン ダイアログボックスの**新規**フィールド グループで、**名称から取得: マッピング (一般)、Litware, Inc.** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-410">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General), Litware, Inc.**.</span></span>
4.  <span data-ttu-id="2f7f1-411">**名前**フィールドに、**マッピング (一般) カスタム**を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-411">In the **Name** field, enter **Mapping (General) custom**.</span></span>
5.  <span data-ttu-id="2f7f1-412">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-412">Select **Create configuration**.</span></span>

<span data-ttu-id="2f7f1-413">この ER コンフィギュレーションのドラフト バージョン 1 を編集する準備ができていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-413">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="2f7f1-414">サンプル モデル マッピングのデザイン</span><span class="sxs-lookup"><span data-stu-id="2f7f1-414">Design a sample model mapping</span></span>

1.  <span data-ttu-id="2f7f1-415">**構成**ページで、**デザイナー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-415">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="2f7f1-416">基本コンフィギュレーションのモデル マッピングがこのコンフィギュレーションに自動的にコピーされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-416">Notice that the model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="2f7f1-417">**マッピング (一般) コピー** マッピングを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-417">Select the **Mapping (General) Copy** mapping.</span></span>
3.  <span data-ttu-id="2f7f1-418">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-418">Select **Designer**.</span></span>
4.  <span data-ttu-id="2f7f1-419">**データ モデル** セクションで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-419">In the **Data model** section, select **Edit**.</span></span>
5.  <span data-ttu-id="2f7f1-420">**式**フィールドに、**一般的な機能 1 カスタム**を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-420">In the **Formula** field, enter **"Generic functionality 1 custom"**.</span></span>
6.  <span data-ttu-id="2f7f1-421">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-421">Select **Save**.</span></span>
7.  <span data-ttu-id="2f7f1-422">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-422">Close the page.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  <span data-ttu-id="2f7f1-424">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-424">Select **Save**.</span></span>
9.  <span data-ttu-id="2f7f1-425">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-425">Close the page.</span></span>
10. <span data-ttu-id="2f7f1-426">**マッピング (一般) 2 コピー** マッピングを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-426">Select the **Mapping (General) 2 Copy** mapping.</span></span>
11. <span data-ttu-id="2f7f1-427">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-427">Select **Designer**.</span></span>
12. <span data-ttu-id="2f7f1-428">**データ モデル** セクションで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-428">In the **Data model** section, select **Edit**.</span></span>
13. <span data-ttu-id="2f7f1-429">**式**フィールドに、**一般的な機能 2 カスタム**を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-429">In the **Formula** field, enter **"Generic functionality 2 custom"**.</span></span>
14. <span data-ttu-id="2f7f1-430">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-430">Select **Save**.</span></span>
15. <span data-ttu-id="2f7f1-431">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-431">Close the page.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. <span data-ttu-id="2f7f1-433">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-433">Select **Save**.</span></span>
17. <span data-ttu-id="2f7f1-434">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-434">Close the page.</span></span>

    ![ER モデル マッピング ページ](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. <span data-ttu-id="2f7f1-436">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-436">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="2f7f1-437">モデル マッピング コンフィギュレーションの変更されたバージョンを完了する</span><span class="sxs-lookup"><span data-stu-id="2f7f1-437">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="2f7f1-438">**バージョン** クイック タブの**コンフィギュレーション** ページで、**ステータスの変更**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-438">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="2f7f1-439">設計されたモデル マッピング コンフィギュレーションのステータスを**ドラフト**から**完了**に変更し、ER 形式で使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-439">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="2f7f1-440">**完了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-440">Select **Complete**.</span></span>
3.  <span data-ttu-id="2f7f1-441">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-441">Select **OK**.</span></span>

<span data-ttu-id="2f7f1-442">作成したコンフィギュレーションが完了したバージョン 1 として保存されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-442">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="appendix3"></a><span data-ttu-id="2f7f1-443">付録 3</span><span class="sxs-lookup"><span data-stu-id="2f7f1-443">Appendix 3</span></span>

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a><span data-ttu-id="2f7f1-444">国/地域固有のカスタマイズのために、サンプル モデル マッピングをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="2f7f1-444">Configure a sample model mapping for country/region-specific customization</span></span>

<span data-ttu-id="2f7f1-445">一部の ER 形式については、データの準備に関する国/地域固有の要件が存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-445">For some ER formats, there might be country/region-specific requirements for data preparation.</span></span> <span data-ttu-id="2f7f1-446">この場合、ER モデル マッピング コンフィギュレーションを個別に管理し、これらの国や地域固有の要件の実装を、一般的な実装から分離することができます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-446">In this case, you can manage a separate ER model mapping configuration and isolate the implementation of these country/region-specific requirements from the general implementation.</span></span> <span data-ttu-id="2f7f1-447">この付録の手順では、**マッピングを知るための形式** ER 形式とフランス固有の要件を例として使用します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-447">The procedures in this appendix use the **Format to learn mappings** ER format and French-specific requirements as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="2f7f1-448">ER モデル マッピング コンフィギュレーションを作成する</span><span class="sxs-lookup"><span data-stu-id="2f7f1-448">Create an ER model mapping configuration</span></span>

<span data-ttu-id="2f7f1-449">最初に、新しい ER モデル マッピング コンフィギュレーションを作成して、国/地域固有の要件を実装します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-449">First, create a new ER model mapping configuration to implement the country/region-specific requirements.</span></span> <span data-ttu-id="2f7f1-450">カスタム ER モデル マッピング コンフィギュレーションをベースとして使用します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-450">Use your custom ER model mapping configuration as a base.</span></span>

1.  <span data-ttu-id="2f7f1-451">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**マッピング (一般) カスタム**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-451">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="2f7f1-452">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-452">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="2f7f1-453">ドロップダウン ダイアログボックスの**新規**フィールド グループで、**名称から取得: マッピング (一般)、Litware, Inc.** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-453">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General) custom, Litware, Inc**.</span></span>
4.  <span data-ttu-id="2f7f1-454">**名前**フィールドに、**マッピング (FR)** を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-454">In the **Name** field, enter **Mapping (FR)**.</span></span>
5.  <span data-ttu-id="2f7f1-455">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-455">Select **Create configuration**.</span></span>

<span data-ttu-id="2f7f1-456">この ER コンフィギュレーションのドラフト バージョン 1 を編集する準備ができていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-456">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="2f7f1-457">サンプル モデル マッピングのデザイン</span><span class="sxs-lookup"><span data-stu-id="2f7f1-457">Design a sample model mapping</span></span>

1.  <span data-ttu-id="2f7f1-458">**構成**ページで、**デザイナー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-458">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="2f7f1-459">基本コンフィギュレーションのモデル マッピングがこのコンフィギュレーションに自動的にコピーされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-459">Notice that model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="2f7f1-460">**マッピング (一般) コピー コピー** マッピングを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-460">Select the **Mapping (General) Copy Copy** mapping.</span></span>
3.  <span data-ttu-id="2f7f1-461">**マッピング (FR)** の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-461">Rename it **Mapping (FR)**.</span></span>
4.  <span data-ttu-id="2f7f1-462">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-462">Select **Designer**.</span></span>
5.  <span data-ttu-id="2f7f1-463">**データ モデル** セクションで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-463">In the **Data model** section, select **Edit**.</span></span>
6.  <span data-ttu-id="2f7f1-464">**式**フィールドに、**FR 機能 1** を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-464">In the **Formula** field, enter **"FR functionality 1"**.</span></span>
7.  <span data-ttu-id="2f7f1-465">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-465">Select **Save**.</span></span>
8.  <span data-ttu-id="2f7f1-466">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-466">Close the page.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  <span data-ttu-id="2f7f1-468">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-468">Select **Save**.</span></span>
10. <span data-ttu-id="2f7f1-469">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-469">Close the page.</span></span>
11. <span data-ttu-id="2f7f1-470">**マッピング (一般) 2 コピー コピー** マッピングを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-470">Select the **Mapping (General) 2 Copy Copy** mapping.</span></span>
12. <span data-ttu-id="2f7f1-471">**マッピング (FR) 2** の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-471">Rename it **Mapping (FR) 2**.</span></span>
13. <span data-ttu-id="2f7f1-472">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-472">Select **Designer**.</span></span>
14. <span data-ttu-id="2f7f1-473">**データ モデル** セクションで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-473">In the **Data model** section, select **Edit**.</span></span>
15. <span data-ttu-id="2f7f1-474">**式**フィールドに、**FR 機能 2** を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-474">In the **Formula** field, enter **"FR functionality 2"**.</span></span>
16. <span data-ttu-id="2f7f1-475">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-475">Select **Save**.</span></span>
17. <span data-ttu-id="2f7f1-476">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-476">Close the page.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. <span data-ttu-id="2f7f1-478">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-478">Select **Save**.</span></span>
19. <span data-ttu-id="2f7f1-479">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-479">Close the page.</span></span>

    ![ER モデル マッピング ページ](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. <span data-ttu-id="2f7f1-481">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-481">Close the page.</span></span>

#### <a name="specify-countryregion-context-restrictions-for-use"></a><span data-ttu-id="2f7f1-482">使用する国/地域のコンテキスト制限の指定</span><span class="sxs-lookup"><span data-stu-id="2f7f1-482">Specify country/region context restrictions for use</span></span>

1.  <span data-ttu-id="2f7f1-483">**ISO 国/地域コード**クイックタブの**コンフィギュレーション**ページで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-483">On the **Configurations** page, on the **ISO Country/region codes** FastTab, select **New**.</span></span>
2.  <span data-ttu-id="2f7f1-484">**ISO** フィールドで、**FR** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-484">In the **ISO** field, select **FR**.</span></span>
3.  <span data-ttu-id="2f7f1-485">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-485">Select **Save**.</span></span>

<span data-ttu-id="2f7f1-486">ER 形式を実行するには、Finance の特定の会社にログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-486">Note that you must sign in to a specific company in Finance to run an ER format.</span></span> <span data-ttu-id="2f7f1-487">したがって、この会社を ER 形式の実行と、基本 ER データ モデルの正しい ER モデル マッピングの選択を管理する当事者と見なすことができます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-487">Therefore, this company can be considered a party that controls both ER format execution and selection of the correct ER model mapping of the base ER data model.</span></span> <span data-ttu-id="2f7f1-488">**FR** 国コードを追加することにより、このモデル マッピングが、フランスの国/地域コンテキストのある会社の管理下で実行される場合にのみ、基本データ モデルの ER 形式に、このモデル マッピングを選択できるように指定します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-488">By adding the **FR** country code, you specify that this model mapping is available for selection by an ER format of the base data model only when that format is run under the control of a company that has French country/region context.</span></span>

<span data-ttu-id="2f7f1-489">ER モデル マッピング コンフィギュレーションの 1 つのバージョンに複数の国/地域コードを追加できます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-489">You can add multiple country/region codes for a single version of an ER model mapping configuration.</span></span> <span data-ttu-id="2f7f1-490">これにより、そのモデル マッピング コンフィギュレーションに存在するモデル マッピングを、異なる国/地域コンテキストのある会社の管理下で実行される ER 形式に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-490">In this way, model mappings that reside in that model mapping configuration can be used for an ER format that is run under the control of companies that have a different country/region context.</span></span>

<span data-ttu-id="2f7f1-491">国/地域コードの一覧は ER モデル マッピング コンフィギュレーションの各バージョンに対して指定されており、バージョンによって異なる場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-491">Note that the list of country/region codes is specified for each version of an ER model mapping configuration and can vary from version to version.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="2f7f1-492">モデル マッピング コンフィギュレーションの変更されたバージョンを完了する</span><span class="sxs-lookup"><span data-stu-id="2f7f1-492">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="2f7f1-493">**バージョン** クイック タブの**コンフィギュレーション** ページで、**ステータスの変更**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-493">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="2f7f1-494">設計されたモデル マッピング コンフィギュレーションのステータスを**ドラフト**から**完了**に変更し、ER 形式で使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-494">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="2f7f1-495">**完了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-495">Select **Complete**.</span></span>
3.  <span data-ttu-id="2f7f1-496">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-496">Select **OK**.</span></span>

<span data-ttu-id="2f7f1-497">作成したコンフィギュレーションが完了したバージョン 1 として保存されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-497">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f7f1-498">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2f7f1-498">Additional resources</span></span>

[<span data-ttu-id="2f7f1-499">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="2f7f1-499">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="2f7f1-500">個別の ER コンフィギュレーションで ER モデル マッピングを管理する</span><span class="sxs-lookup"><span data-stu-id="2f7f1-500">Manage ER model mapping in separate ER configurations</span></span>](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[<span data-ttu-id="2f7f1-501">国/地域コンテキストの適用</span><span class="sxs-lookup"><span data-stu-id="2f7f1-501">Apply country/region context</span></span>](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="2f7f1-502">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="2f7f1-502">Frequently asked questions</span></span>

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a><span data-ttu-id="2f7f1-503">RCS で 2 つの共有 ER モデル マッピング コンフィギュレーションをコンフィギュレーションし、そのうちの 1 つを既定のモデル マッピングのコンフィギュレーションとしてマークしました。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-503">I configured two shared ER model mapping configurations in RCS and marked one of them as the default model mapping configuration.</span></span> <span data-ttu-id="2f7f1-504">同じ基本 ER データ モデル コンフィギュレーションに対して作成された ER 形式を、テスト モデル マッピングに対して正常に実行しました。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-504">I successfully ran an ER format that was created for the same base ER data model configuration, to test model mappings.</span></span> <span data-ttu-id="2f7f1-505">次に、ER ソリューション全体 (ER データ モデル、2 つの ER マッピング コンフィギュレーション、および ER 形式コンフィギュレーション) を Finance にインポートしました。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-505">I then imported the whole ER solution (ER data model, two ER model mapping configurations, and ER format configuration) into Finance.</span></span> <span data-ttu-id="2f7f1-506">Finance で同じ ER 形式を実行しようとすると、エラーメッセージが表示されるのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-506">Why do I receive an error message when I try to run the same ER format in Finance?</span></span>
<span data-ttu-id="2f7f1-507">既定のモデル マッピングの設定は、環境に固有です。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-507">The default model mapping setting is environment-specific.</span></span> <span data-ttu-id="2f7f1-508">RCS でコンフィギュレーションされていますが、Finance にはエクスポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-508">It's configured in RCS but isn't exported to Finance.</span></span> <span data-ttu-id="2f7f1-509">この ER 形式を正常に実行するには、ER モデル マッピングのコンフィギュレーションのいずれかを、Finance の既定のモデル マッピング コンフィギュレーションとしてマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-509">To successfully run this ER format, you must mark one of ER model mapping configurations as the default model mapping configuration in Finance too.</span></span>

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a><span data-ttu-id="2f7f1-510">1 つのモデル マッピングを共有モデル マッピングとしてコンフィギュレーションし、それをドラフト バージョンにしました。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-510">I configured one model mapping as a shared model mapping and completed the draft version of it.</span></span> <span data-ttu-id="2f7f1-511">次に、同じデータ モデルに対して新しいモデル マッピング コンフィギュレーションを追加し、フランス固有のモデルをコンフィギュレーションしました。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-511">I then added a new model mapping configuration for same data model and configured it as French-specific.</span></span> <span data-ttu-id="2f7f1-512">この ER 形式では正しいルート定義が使用されており、フランスの国/地域コンテキストのある会社の管理下で実行が行われているのに、ER 形式を実行すると共有モデル マッピングが選択されるのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-512">Why is the shared model mapping selected when I run an ER format, even though this ER format uses the correct root definition and execution is done under the control of the company that has French country/region context?</span></span>
<span data-ttu-id="2f7f1-513">共有モデル マッピング コンフィギュレーションが既定のモデル マッピング コンフィギュレーションとしてマークされていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-513">Make sure that the shared model mapping configuration isn't marked as the default model mapping configuration.</span></span> <span data-ttu-id="2f7f1-514">それ以外の場合は、マッピングの選択時に優先順位が高くなります。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-514">Otherwise, it will have higher priority during mapping selection.</span></span> <span data-ttu-id="2f7f1-515">また、ER 形式の実行中にマッピングが選択されている場合は、フランス固有のモデル マッピング コンフィギュレーションが考慮されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-515">Also make sure that the French-specific model mapping configuration is considered when a mapping is selected during ER format execution.</span></span> <span data-ttu-id="2f7f1-516">ER モデル マッピング コンフィギュレーションは、次の条件のうち少なくとも 1 つを満たす場合にのみ選択できます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-516">An ER model mapping configuration is available for selection only if at least one of the following conditions is met:</span></span>
- <span data-ttu-id="2f7f1-517">ER モデル マッピング コンフィギュレーションの少なくとも 1 つのバージョンが**完了**しているか、**共有**ステータスになっています。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-517">At least one version of the ER model mapping configuration has either **Completed** or **Shared** status.</span></span> <span data-ttu-id="2f7f1-518">この場合は、バージョン番号が最も大きいバージョンが ER 形式の実行に使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-518">In this case, the version that has the highest version number will be used for ER format execution.</span></span>
- <span data-ttu-id="2f7f1-519">ER モデル マッピング コンフィギュレーションの**ドラフトの実行**オプションがオンになっています。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-519">The **Run draft** option for the ER model mapping configuration is turned on.</span></span> <span data-ttu-id="2f7f1-520">この場合は、**ドラフト** 状態のバージョンが ER 形式の実行に使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-520">In this case, the version that has **Draft** status will be used for ER format execution.</span></span>
> <span data-ttu-id="2f7f1-521">**ドラフトの実行**オプションは、**実行設定**のユーザーパラメータがオンになっている場合に、各 ER モデル マッピング コンフィギュレーションの**コンフィギュレーション** ページで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="2f7f1-521">The **Run draft** option becomes available on the **Configurations** page for each ER model mapping configuration when the **Run setting** ER user parameter is turned on.</span></span>
