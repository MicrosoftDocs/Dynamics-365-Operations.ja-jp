---
title: 電子申告における多言語レポートの設計
description: このトピックでは、電子申告 (ER) ラベルを使用して多言語レポートをデザインおよび生成する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7934f36877247460ec843201a08d4670456889f9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679705"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a><span data-ttu-id="98746-103">電子申告における多言語レポートの設計</span><span class="sxs-lookup"><span data-stu-id="98746-103">Design multilingual reports in Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="98746-104">概要</span><span class="sxs-lookup"><span data-stu-id="98746-104">Overview</span></span>

<span data-ttu-id="98746-105">ビジネス ユーザーとして、[電子申告 (ER)](general-electronic-reporting.md) フレームワークを使用し、さまざまな国や地域の法的要件に従って生成されなければならない送信ドキュメントの形式を構成できます。</span><span class="sxs-lookup"><span data-stu-id="98746-105">As a business user, you can use the [Electronic reporting (ER)](general-electronic-reporting.md) framework to configure formats for outbound documents that must be generated in accordance with the legal requirements of various countries or regions.</span></span> <span data-ttu-id="98746-106">これらの要件により、送信ドキュメントを国や地域ごとに異なる言語で生成する必要がある場合は、言語依存のリソースを含む 1 つの ER [形式](general-electronic-reporting.md#FormatComponentOutbound) を構成できます。</span><span class="sxs-lookup"><span data-stu-id="98746-106">When these requirements demand that outbound documents be generated in different languages for different countries or regions, you can configure a single ER [format](general-electronic-reporting.md#FormatComponentOutbound) that contains language-dependent resources.</span></span> <span data-ttu-id="98746-107">このようにすると、この形式を再利用してさまざまな国や地域の送信ドキュメントを生成できます。</span><span class="sxs-lookup"><span data-stu-id="98746-107">In that way, you can reuse the format to generate outbound documents for various countries or regions.</span></span> <span data-ttu-id="98746-108">また、1 つの ER 形式を使用して、対応する顧客、仕入先、関連会社、またはその他の関係者向けに、送信ドキュメントを異なる言語で生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="98746-108">You might also want to use a single ER format to generate an outbound document in different languages for corresponding customers, vendors, subsidiaries, or any other parties.</span></span>

<span data-ttu-id="98746-109">ER データ モデルとモデル マッピングを構成済み ER 形式のデータソースとして構成し、生成されたドキュメントに挿入するアプリケーション データを指定するデータ フローを定義できます。</span><span class="sxs-lookup"><span data-stu-id="98746-109">You can configure ER data models and model mappings as the data sources of configured ER formats to define the data flow that specifies what application data is put into generated documents.</span></span> <span data-ttu-id="98746-110">ER コンフィギュレーション [プロバイダー](general-electronic-reporting.md#Provider)として 、構成済みの [データ モデル](general-electronic-reporting.md#data-model-and-model-mapping-components)、[モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components)、および [形式](general-electronic-reporting.md#FormatComponentOutbound) を ER ソリューションのコンポーネントとして [公開](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) し、特定の送信ドキュメントを生成できます。</span><span class="sxs-lookup"><span data-stu-id="98746-110">As an ER configuration [provider](general-electronic-reporting.md#Provider), you can [publish](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) configured [data models](general-electronic-reporting.md#data-model-and-model-mapping-components), [model mappings](general-electronic-reporting.md#data-model-and-model-mapping-components), and [formats](general-electronic-reporting.md#FormatComponentOutbound) as components of an ER solution to generate specific outbound documents.</span></span> <span data-ttu-id="98746-111">公開された ER ソリューションを顧客が [アップロード](general-electronic-reporting-manage-configuration-lifecycle.md) して、使用およびカスタマイズできるようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="98746-111">You can also allow customers to [upload](general-electronic-reporting-manage-configuration-lifecycle.md) the published ER solution so that it can be used and customized.</span></span> <span data-ttu-id="98746-112">顧客が他の言語を話す可能性がある場合は、言語依存のリソースを含むように ER コンポーネントを構成できます。</span><span class="sxs-lookup"><span data-stu-id="98746-112">If you expect that customers might speak other languages, you can configure the ER components so that they contain language-dependent resources.</span></span> <span data-ttu-id="98746-113">このようにして、設計時に、編集可能な ER コンポーネントのコンテンツを顧客のユーザー優先言語で表示できます。</span><span class="sxs-lookup"><span data-stu-id="98746-113">In that way, the content of an editable ER component can be presented in a customer's user-preferred language at design time.</span></span>

<span data-ttu-id="98746-114">言語依存のリソースを ER ラベルとして構成できます。</span><span class="sxs-lookup"><span data-stu-id="98746-114">You can configure language-dependent resources as ER labels.</span></span> <span data-ttu-id="98746-115">これらのラベルを使用して、ER コンポーネントを次の目的で構成できます:</span><span class="sxs-lookup"><span data-stu-id="98746-115">You can then use those labels to configure ER components for the following purposes:</span></span>

- <span data-ttu-id="98746-116">設計時に:</span><span class="sxs-lookup"><span data-stu-id="98746-116">At design time:</span></span>

    - <span data-ttu-id="98746-117">構成済み ER コンポーネントのコンテンツを、ユーザーの優先言語で表示します。</span><span class="sxs-lookup"><span data-stu-id="98746-117">Present the content of configured ER components in the user-preferred language.</span></span>

- <span data-ttu-id="98746-118">ランタイムに:</span><span class="sxs-lookup"><span data-stu-id="98746-118">At runtime:</span></span>

    - <span data-ttu-id="98746-119">送信ドキュメントの言語依存コンテンツを生成します。</span><span class="sxs-lookup"><span data-stu-id="98746-119">Generate language-dependent content for outbound documents.</span></span>
    - <span data-ttu-id="98746-120">ユーザーの優先言語で警告とエラー メッセージを提供します。</span><span class="sxs-lookup"><span data-stu-id="98746-120">Provide warning and error messages in the user-preferred language.</span></span>
    - <span data-ttu-id="98746-121">ユーザーの優先言語で必須フィールドの入力を促します。</span><span class="sxs-lookup"><span data-stu-id="98746-121">Prompt for required fields in the user-preferred language.</span></span>

<span data-ttu-id="98746-122">ER ラベルは、異なるコンポーネントを含むすべての ER [コンフィギュレーション](general-electronic-reporting.md#Configuration) で構成できます。</span><span class="sxs-lookup"><span data-stu-id="98746-122">ER labels can be configured in every ER [configuration](general-electronic-reporting.md#Configuration) that contains different components.</span></span> <span data-ttu-id="98746-123">ラベルは、ER データ モデル、ER モデル マッピング、および ER 形式コンポーネントの構成されたロジックとは別に管理できます。</span><span class="sxs-lookup"><span data-stu-id="98746-123">The labels can be maintained independently of the configured logic of ER data models, ER model mappings, and ER format components.</span></span>

<span data-ttu-id="98746-124">すべての ER ラベルは、そのラベルを保持する ER コンフィギュレーションの範囲内で一意の ID によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="98746-124">Every ER label is identified by an ID that is unique in the scope of the ER configuration that holds that label.</span></span> <span data-ttu-id="98746-125">すべてのラベルに、Microsoft Dynamics 365 Finance の現在のインスタンスでサポートされているすべての言語のラベル テキストを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="98746-125">Every label can contain label text for every language that is supported in the current instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="98746-126">これらのサポートされている言語には、配置されたカスタマイズの言語が含まれます。</span><span class="sxs-lookup"><span data-stu-id="98746-126">These supported languages include the languages of deployed customizations.</span></span>

## <a name="entry"></a><span data-ttu-id="98746-127">入力</span><span class="sxs-lookup"><span data-stu-id="98746-127">Entry</span></span>

<span data-ttu-id="98746-128">ER データ モデル、ER モデル マッピング、または ER 形式を設計する場合、翻訳可能なコンテキストを含む可能性のあるフィールドを選択すると、**翻訳** オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="98746-128">When you design an ER data model, an ER model mapping, or an ER format, the **Translate** option is shown whenever you select a field that might contain the translatable context.</span></span> <span data-ttu-id="98746-129">このオプションを選択すると、選択したフィールドを **テキストの翻訳** <a name="TextTranslationPane">ペイン</a> で ER ラベルにリンクできます。</span><span class="sxs-lookup"><span data-stu-id="98746-129">When you select this option, you can link the selected field to an ER label on the **Text translation** <a name="TextTranslationPane">pane</a>.</span></span> <span data-ttu-id="98746-130">既存の ER ラベルを選択することも、まだ使用できない場合は新しい ER ラベルを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="98746-130">You can select an existing ER label, or you can add a new ER label if it isn't available yet.</span></span> <span data-ttu-id="98746-131">ER ラベルを選択または追加すると、現在の Finance インスタンスでサポートされているすべての言語について、関連するテキストを追加できます。</span><span class="sxs-lookup"><span data-stu-id="98746-131">When you select or add an ER label, you can add related text for every language that is supported in the current Finance instance.</span></span>

<span data-ttu-id="98746-132">次の図は、編集可能な ER データ モデルで、この翻訳がどのように行われるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="98746-132">The following illustration shows how this translation is done in an editable ER data model.</span></span> <span data-ttu-id="98746-133">この例では、編集可能な **請求書モデル** の **PurchaseOrder** フィールドの **説明** 属性 が、オーストリアのドイツ語 (DE-AT) および日本語 (JA) に翻訳されています。</span><span class="sxs-lookup"><span data-stu-id="98746-133">In this example, the **Description** attribute of the **PurchaseOrder** field for the editable **Invoice model** is translated into the Austrian German (DE-AT) and Japanese (JA) languages.</span></span>

![ER データ モデル デザイナーで ER ラベルの翻訳を提供する](./media/er-multilingual-labels-refer.png)

<span data-ttu-id="98746-135">編集可能な ER コンポーネントにあるラベルのラベル テキストのみ翻訳することができます。</span><span class="sxs-lookup"><span data-stu-id="98746-135">Only label text for labels that reside in an editable ER component can be translated.</span></span> <span data-ttu-id="98746-136">たとえば、ER モデル マッピング データ ソースのラベル属性に **翻訳** を選択し、親 ER データ モデルにある ER ラベルを選択すると、ラベルのコンテンツが表示されますが、変更はできません。</span><span class="sxs-lookup"><span data-stu-id="98746-136">For example, if you select **Translate** for the label attribute of an ER model mapping data source, and you then select an ER label that resides in the parent ER data model, you will see the content of the label, but you can't change it.</span></span> <span data-ttu-id="98746-137">この場合、次の図に示すように、**翻訳テキス** フィールドは使用できません。</span><span class="sxs-lookup"><span data-stu-id="98746-137">In these cases, the **Translated text** field is unavailable, as shown in the following illustration.</span></span>

![ER モデル マッピング デザイナーで提供された ER ラベルの翻訳を確認する](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> <span data-ttu-id="98746-139">デザイナーを使用して編集可能な ER コンポーネントに入力されたラベルを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="98746-139">You can't use the designers to delete label that has been entered in an editable ER component.</span></span>

## <a name="scope"></a><span data-ttu-id="98746-140">スコープ</span><span class="sxs-lookup"><span data-stu-id="98746-140">Scope</span></span>

<span data-ttu-id="98746-141">ER ラベルは、ER コンポーネントのいくつかの翻訳可能な属性で参照できます。</span><span class="sxs-lookup"><span data-stu-id="98746-141">ER labels can be referred to in several translatable attributes of ER components.</span></span>

### <a name="data-model-component"></a><span data-ttu-id="98746-142">データ モデル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="98746-142">Data model component</span></span>

<span data-ttu-id="98746-143">ER データ モデルを構成するときに、そのデータ モデルに ER ラベルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="98746-143">When you configure an ER data model, you can add ER labels for it.</span></span> <span data-ttu-id="98746-144">モデル項目の **ラベル** と **説明** の属性、すべてのモデルのフィールド、およびすべての <a id="LinkModelEnum"></a>モデル列挙値は、ER データ モデルに追加される ER ラベルにリンクできます。</span><span class="sxs-lookup"><span data-stu-id="98746-144">**Label** and **Description** attributes of the model item, every model's field, and every <a id="LinkModelEnum"></a>model enumeration value can be linked to an ER label that is added to the ER data model.</span></span>

![ER データ モデル デザイナーで説明属性の翻訳を提供する](./media/er-multilingual-labels-refer.png)

<span data-ttu-id="98746-146">ER データ モデルがこのように構成されている場合、そのコンテンツは ER データ モデル デザイナーのユーザーに各ユーザーの優先言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="98746-146">When an ER data model is configured in this way, its content will be presented to users of the ER data model designer in each user's preferred language.</span></span> <span data-ttu-id="98746-147">したがって、モデル メンテナンスが簡略化されます。</span><span class="sxs-lookup"><span data-stu-id="98746-147">Therefore, model maintenance is simplified.</span></span> <span data-ttu-id="98746-148">次の図は、DE-AT および JA を優先言語として設定しているユーザーに対して、この機能がどのように機能するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="98746-148">The following illustrations show how this functionality works for users who have DE-AT and JA set as their preferred language.</span></span>

![DE-AT を優先言語として設定しているユーザーのための ER データ モデル デザイナー レイアウト](./media/er-multilingual-labels-refer-de.png)

![JA を優先言語として設定しているユーザーのための ER データ モデル デザイナー レイアウト](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a><span data-ttu-id="98746-151">モデル マッピング コンポーネント</span><span class="sxs-lookup"><span data-stu-id="98746-151">Model mapping component</span></span>

<span data-ttu-id="98746-152">ER モデル マッピングは ER データ モデルに基づいているため、参照されるデータ モデル要素のラベルは、モデル マッピング デザイナーのユーザーの優先言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="98746-152">Because the ER model mapping is based on an ER data model, the labels of the data model elements that are referred to are appeared in the user's preferred language in the model mapping designer.</span></span> <span data-ttu-id="98746-153">次の図は、**PurchaseOrder** フィールドの意味が、構成済みデータ モデルに追加された **説明** 属性のラベルを使用して、編集可能なモデル マッピングでどのように説明されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="98746-153">The following illustration shows how the meaning of the **PurchaseOrder** field is explained in the editable model mapping by using the label of the **Description** attribute that has been added to the configured data model.</span></span> <span data-ttu-id="98746-154">このラベルは、ユーザーの優先言語 (この例では DE-AT) で表示されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="98746-154">Notice that this label is presented in the user's preferred language (DE-AT in this example).</span></span>

![DE-AT を優先言語として設定しているユーザーのための ER モデル マッピング デザイナー レイアウト](./media/er-multilingual-labels-show-mapping.png)

<span data-ttu-id="98746-156">**ユーザー 入力 パラメータ** データ ソースの **ラベル** 属性が ER ラベルにリンクするように構成されている場合、このデータ ソースに対応するパラメータ フィールドは、ランタイムにユーザーの優先言語でユーザー ダイアログ ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="98746-156">When the **Label** attribute of the **User input parameter** data source is configured as linked to an ER label, the parameter field that corresponds to this data source is presented in the user dialog box at runtime to users in their preferred language.</span></span>

### <a name="format-component"></a><span data-ttu-id="98746-157">形式コンポーネント</span><span class="sxs-lookup"><span data-stu-id="98746-157">Format component</span></span>

<span data-ttu-id="98746-158">ER 形式を構成するときに、その形式に ER ラベルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="98746-158">When you configure an ER format, you can add ER labels for it.</span></span> <span data-ttu-id="98746-159">すべての構成済みデータ ソースの **ラベル** と **ヘルプ テキスト** 属性は、ER 形式に追加される ER ラベルにリンクできます。</span><span class="sxs-lookup"><span data-stu-id="98746-159">The **Label** and **Help text** attributes of every configured data source can be linked to an ER label that is added to the ER format.</span></span> <span data-ttu-id="98746-160">すべての <a id="LinkFormatEnum"></a>形式列挙値の **ラベル** および **説明** 属性は、編集可能な ER 形式からアクセス可能な ER ラベルにリンクすることもできます。</span><span class="sxs-lookup"><span data-stu-id="98746-160">The **Label** and **Description** attributes of every <a id="LinkFormatEnum"></a>format enumeration value can be also linked to an ER label that is accessible from the editable ER format.</span></span>

> [!NOTE]
> <span data-ttu-id="98746-161">これらの属性は、この ER データ モデルに対して構成されているすべての ER 形式でモデルのラベルを再利用する親 ER データ モデルにリンクすることもできます。</span><span class="sxs-lookup"><span data-stu-id="98746-161">You can also link these attributes to an ER label of the parent ER data model that reuses the model's labels in every ER format that is configured for this ER data model.</span></span>

<span data-ttu-id="98746-162">ER 形式がこのように構成されている場合、形式のコンテンツは ER オペレーション デザイナーのユーザーに各ユーザーの優先言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="98746-162">When an ER format is configured in this way, the content of the format will be presented to users of the ER Operation designer in each user's preferred language.</span></span> <span data-ttu-id="98746-163">したがって、構成されたロジックの形式のメンテナンスと分析が簡略化されます。</span><span class="sxs-lookup"><span data-stu-id="98746-163">Therefore, format maintenance and analysis of the configured logic are simplified.</span></span>

<span data-ttu-id="98746-164">ER 形式は ER データ モデルに基づいているため、データ モデル要素で参照されるラベルは、ER 形式デザイナーでユーザーの優先言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="98746-164">Because an ER format is based on an ER data model, the labels that are referred to in the data model elements are presented in the ER format designer in the user-preferred language.</span></span>

<span data-ttu-id="98746-165">**ユーザー 入力 パラメータ** データ ソースの **ラベル** 属性が ER ラベルにリンクされている場合、ランタイムにユーザー ダイアログ ボックスのパラメータに対応するフィールドがプロンプトとしてユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="98746-165">When the **Label** attribute of the **User input parameter** data source is linked to an ER label, the field that corresponds to the parameter in the user dialog box at runtime is presented to the user as a prompt.</span></span> <span data-ttu-id="98746-166">次の図は、設計時に **ユーザー入力パラメータ** データソースの **ラベル** 属性を ER ラベルにリンクして、ユーザーが、ランタイムに異なる優先言語 (米国英語 (EN-US) と DE-AT 言語で表示) でパラメータの入力を促すようにする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="98746-166">The following illustrations show how you can link the **Label** attribute of the **User input parameter** data source at design time to an ER label, so that users are prompted for the parameter in different user-preferred languages (shown for English United States (EN-US) and DE-AT languages) at runtime.</span></span>

![ER オペレーション デザイナーでユーザー入力パラメータ属性の翻訳を提供する](./media/er-multilingual-labels-refer-format.png)

![EN-US ユーザー優先言語ランタイムの ER 仕入先支払い処理](./media/er-multilingual-labels-show-runtime-en.png)

![DE-AT ユーザー優先言語のランタイムの ER 仕入先支払い処理](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a><span data-ttu-id="98746-170">式</span><span class="sxs-lookup"><span data-stu-id="98746-170">Expressions</span></span>

<span data-ttu-id="98746-171">ER [式](er-formula-language.md) でラベルを使用するには、構文 **@"GER\_LABEL:X"** を使用する必要があります。接頭語 **@** はオペランドがラベルを参照していることを示し、**GER\_LABEL** は ER ラベルが関係することを示し、**X** は ER ラベル ID です。</span><span class="sxs-lookup"><span data-stu-id="98746-171">To use a label in an ER [expression](er-formula-language.md), you must use the syntax **@"GER\_LABEL:X"**, where the prefix **@** indicates that the operand refers to a label, **GER\_LABEL** indicates that an ER label is involved, and **X** is the ER label ID.</span></span>

![ER フォーミュラ デザイナーで ER ラベルへの参照を含む ER 式を構成する](./media/er-multilingual-labels-expression1.png)

<span data-ttu-id="98746-173">システム (アプリケーション) ラベルを参照するには、構文 **@"X"** を使用します。接頭語 **@** はオペランドがラベルを参照し、**X** がシステム ラベル ID であることを示します。</span><span class="sxs-lookup"><span data-stu-id="98746-173">To refer to a system (application) label, use the syntax **@"X"**, where the prefix **@** indicates that the operand refers to a label, and **X** is the system label ID.</span></span>

![ER フォーミュラ デザイナーでアプリケーション ラベルへの参照を含む ER 式を構成する](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a><span data-ttu-id="98746-175">モデル マッピング</span><span class="sxs-lookup"><span data-stu-id="98746-175">Model mapping</span></span>

<span data-ttu-id="98746-176">ER モデル マッピングの式は、ラベルを使用して構成できます。</span><span class="sxs-lookup"><span data-stu-id="98746-176">An expression of an ER model mapping can be configured by using a label.</span></span> <span data-ttu-id="98746-177">このマッピングが、送信ドキュメントを生成するために実行される ER 形式によって呼び出される場合、実行のコンテキストには言語コードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="98746-177">When this mapping is called by an ER format that is run to generate an outbound document, the context of the execution includes a language code.</span></span> <span data-ttu-id="98746-178">構成済みの式ラベルには、そのコンテキストの言語に対して構成されたラベル テキストが入力されます。</span><span class="sxs-lookup"><span data-stu-id="98746-178">A configured expression label will be filled in with the label text that has been configured for the language of that context.</span></span>

<span data-ttu-id="98746-179">参照されるラベルが、モデル マッピングを呼び出す形式の実行コンテキストの言語に翻訳されていない場合、EN-US 言語のラベル テキストが代わりに使用されます。</span><span class="sxs-lookup"><span data-stu-id="98746-179">If a referenced label has no translation for the language of the format execution context that calls the model mapping, the label text in the EN-US language is used instead.</span></span>

#### <a name="format"></a><span data-ttu-id="98746-180">書式設定</span><span class="sxs-lookup"><span data-stu-id="98746-180">Format</span></span>

<span data-ttu-id="98746-181">ER 形式の式は、ラベルを使用して構成できます。</span><span class="sxs-lookup"><span data-stu-id="98746-181">An ER expression of an ER format can be configured by using labels.</span></span> <span data-ttu-id="98746-182">この形式を実行して送信ドキュメントを生成すると、実行のコンテキストには言語コードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="98746-182">When this format is run to generate an outbound document, the context of the execution includes a language code.</span></span> <span data-ttu-id="98746-183">構成済みの式ラベルには、そのコンテキストの言語に対して構成されたラベル テキストが入力されます。</span><span class="sxs-lookup"><span data-stu-id="98746-183">A configured expression label will be filled in with the label text that has been configured for the language of that context.</span></span>

![ER フォーミュラ デザイナーで編集可能な ER 式の ER ラベルの翻訳を提供する](./media/er-multilingual-labels-refer-in-expression.png)

![ER オペレーション デザイナーで ER ラベルを参照するデータ バインディングのサンプル](./media/er-multilingual-labels-refer-in-binding.png)

<span data-ttu-id="98746-186">ER 形式の **ファイル** コンポーネントを構成して、ユーザーの優先言語でレポートを生成できます。</span><span class="sxs-lookup"><span data-stu-id="98746-186">You can configure the **FILE** component of an ER format to generate the report in the user's preferred language.</span></span>

![ユーザーの優先言語でレポートを生成するために ER オペレーション デザイナーのファイル コンポーネントを設定する](./media/er-multilingual-labels-language-context-user.png)

<span data-ttu-id="98746-188">このように ER フォーマットを構成すると、ER ラベルの対応するテキストを使用してレポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="98746-188">If you configure an ER format in this way, the report is generated by using the corresponding text of the ER labels.</span></span> <span data-ttu-id="98746-189">次の図は、EN-US および DE-AT ユーザー言語のレポートの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="98746-189">The following illustrations show examples of reports for the EN-US and DE-AT user languages.</span></span>

![ユーザーの優先言語 EN-US で生成されたレポートのプレビュー](./media/er-multilingual-labels-report-preview-en.png)

![ユーザーの優先言語 DE-AT で生成されたレポートのプレビュー](./media/er-multilingual-labels-report-preview-de.png)

<span data-ttu-id="98746-192">参照されるラベルが、形式の実行コンテキストの言語に翻訳されていない場合、EN-US 言語のラベル テキストが代わりに使用されます。</span><span class="sxs-lookup"><span data-stu-id="98746-192">If a referenced label has no translation for the language of the format execution context, the label text in the EN-US language is used instead.</span></span>

## <a name="language"></a><span data-ttu-id="98746-193">言語</span><span class="sxs-lookup"><span data-stu-id="98746-193">Language</span></span>

<span data-ttu-id="98746-194">ERでは、生成されるレポートの言語を指定するさまざまな方法をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="98746-194">ER supports different ways to specify a language for a generated report.</span></span> <span data-ttu-id="98746-195">**形式** タブの **言語の詳細設定** フィールドで、次の値を選択できます:</span><span class="sxs-lookup"><span data-stu-id="98746-195">In the **Language preferences** field on the **Format** tab, you can select the following values:</span></span>

- <span data-ttu-id="98746-196">**会社の基本設定** – 会社指定の言語でレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="98746-196">**Company preference** – Generate a report in a company-specified language.</span></span>

    ![ER オペレーション デザイナーで、生成されたレポートの言語として会社の優先言語を指定します](./media/er-multilingual-labels-language-context-company.png)

- <span data-ttu-id="98746-198">**ユーザーの基本設定** – ユーザーの優先言語でレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="98746-198">**User preference** – Generate a report in the user's preferred language.</span></span>
- <span data-ttu-id="98746-199">**明示的に定義** – 設計時に指定された言語でレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="98746-199">**Explicitly defined** – Generate a report in a language that is specified at design time.</span></span>

    ![ER オペレーション デザイナーで、生成されたレポートの言語として設計時に定義された言語を指定します](./media/er-multilingual-labels-language-context-fixed.png)

- <span data-ttu-id="98746-201">**ランタイムに定義** – ランタイムに指定された言語でレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="98746-201">**Defined at run-time** – Generate a report in a language that is specified at runtime.</span></span> <span data-ttu-id="98746-202">この値を選択する場合は、**言語** フィールドで、対応する顧客の言語など、言語の言語コードを返す ER 式を構成します。</span><span class="sxs-lookup"><span data-stu-id="98746-202">If you select this value, in the **Language** field, configure an ER expression that returns the language code for the language, such as the language of the corresponding customer.</span></span>

    ![ER オペレーション デザイナーで、生成されたレポートの言語としてランタイム定義言語を指定します](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="translation"></a><span data-ttu-id="98746-204">翻訳</span><span class="sxs-lookup"><span data-stu-id="98746-204">Translation</span></span>

<span data-ttu-id="98746-205">編集可能な ER コンポーネントに必須の ERラ ベルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="98746-205">You can add required ER labels to an editable ER component.</span></span> <span data-ttu-id="98746-206">ER ラベルを追加する場合は、手動と自動の 2 つの方法で翻訳できます。</span><span class="sxs-lookup"><span data-stu-id="98746-206">When an ER label is added, it can be translated in two ways: manually and automatically.</span></span>

### <a name="manual-translation"></a><span data-ttu-id="98746-207">手動翻訳</span><span class="sxs-lookup"><span data-stu-id="98746-207">Manual translation</span></span>

<span data-ttu-id="98746-208">**テキストの翻訳** [ペイン](#TextTranslationPane) に ER ラベルを追加すると、現在の Finance インスタンスでサポートされているすべての言語に手動で翻訳できます。</span><span class="sxs-lookup"><span data-stu-id="98746-208">When you add an ER label on the **Text translation** [pane](#TextTranslationPane), you can manually translate it into all languages that are supported in the current Finance instance.</span></span> <span data-ttu-id="98746-209">**システム言語** または **ユーザー言語** セクションの **言語** フィールドで、優先言語を選択し、対応する **翻訳テキスト** フィールドに適切なテキストを入力して、**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="98746-209">You can select the preferred language in the **Language** field in the **System language** or **User language** section, enter the appropriate text in the corresponding **Translated text** field, and then select **Translate**.</span></span> <span data-ttu-id="98746-210">このプロセスは、追加する必要なすべての言語とすべてのラベルに対して繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="98746-210">This process must be repeated for every required language and every label that you add.</span></span>

### <a name="automatic-translation"></a><span data-ttu-id="98746-211">自動翻訳</span><span class="sxs-lookup"><span data-stu-id="98746-211">Automatic translation</span></span>

<span data-ttu-id="98746-212">ER コンポーネントの構成は、編集可能な ER コンポーネントが存在する ER コンフィギュレーションのドラフト バージョンで行われます。</span><span class="sxs-lookup"><span data-stu-id="98746-212">Configuration of an ER component is done in the draft version of the ER configuration that the editable ER component resides in.</span></span>

![ドラフト ステータスのコンフィギュレーション バージョンにアクセスできる ER コンフィギュレーション ページ](./media/er-multilingual-labels-configurations.png)

<span data-ttu-id="98746-214">このトピックで既に説明したように、必須の ER ラベルを編集可能な ER コンポーネントに追加できます。</span><span class="sxs-lookup"><span data-stu-id="98746-214">As described earlier in this topic, you can add required ER labels to an editable ER component.</span></span> <span data-ttu-id="98746-215">このようにして、ER ラベルのテキストを EN-US 言語で指定できます。</span><span class="sxs-lookup"><span data-stu-id="98746-215">In this way, you can specify the text of the ER labels in the EN-US language.</span></span> <span data-ttu-id="98746-216">その後、組み込み ER 関数を使用して ER コンポーネントのラベルをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="98746-216">You can then export the labels of the ER component by using the built-in ER function.</span></span> <span data-ttu-id="98746-217">編集可能な ER コンポーネントを含む ER コンフィギュレーションのドラフト バージョンを選択し、**交換 \> ラベルのエクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="98746-217">Select the draft version of an ER configuration that contains the editable ER component, and then select **Exchange \> Export labels**.</span></span>

![選択したコンフィギュレーション バージョンから ER ラベルをエクスポートできる ER コンフィギュレーション ページ](./media/er-multilingual-labels-export.png)

<span data-ttu-id="98746-219">すべてのラベルまたはエクスポートの開始時に指定した 1 つの言語のラベルをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="98746-219">You can export either all labels or the labels for a single language that you specify at the beginning of export.</span></span> <span data-ttu-id="98746-220">ラベルは、XML ファイルを含む zip ファイルとしてエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="98746-220">Labels are exported as a zip file that contains XML files.</span></span> <span data-ttu-id="98746-221">すべての XML ファイルには、1 つの言語のラベルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="98746-221">Every XML file contains labels for a single language.</span></span>

![DE-AT 言語用の ER ラベルを含むエクスポート ファイルのサンプル](./media/er-multilingual-labels-in-xml.png)

<span data-ttu-id="98746-223">この形式は、[Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md) などの外部翻訳サービスによるラベルの自動翻訳に使用されます。</span><span class="sxs-lookup"><span data-stu-id="98746-223">This format is used for automatic translation of labels by  external translation services such as [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md).</span></span> <span data-ttu-id="98746-224">翻訳済ラベルを受け取ったら、ラベルを所有する ER コンポーネントを含む ER コンフィギュレーションのドラフト バージョンにインポートできます。</span><span class="sxs-lookup"><span data-stu-id="98746-224">When you receive the translated labels, you can import them back into the draft version of an ER configuration that contains the ER components that own those labels.</span></span> <span data-ttu-id="98746-225">編集可能な ER コンポーネントを含む ER コンフィギュレーションのドラフト バージョンを選択し、**交換 \> ラベルの読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="98746-225">Select the draft version of an ER configuration that contains the editable ER component, and select **Exchange \> Load labels**.</span></span>

![選択したコンフィギュレーション バージョンに ER ラベルをインポートできる ER コンフィギュレーション ページ](./media/er-multilingual-labels-load.png)

<span data-ttu-id="98746-227">翻訳済ラベルは選択した ER コンフィギュレーションにインポートされます。</span><span class="sxs-lookup"><span data-stu-id="98746-227">Translated labels will be imported into the selected ER configuration.</span></span> <span data-ttu-id="98746-228">この ER コンフィギュレーションに存在する翻訳済ラベルは置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="98746-228">Translated labels that exist in this ER configuration are replaced.</span></span> <span data-ttu-id="98746-229">ER コンフィギュレーションに翻訳済ラベルがない場合は追加されます。</span><span class="sxs-lookup"><span data-stu-id="98746-229">If any translated label is missing in the ER configuration, it's appended.</span></span>

## <a name="lifecycle"></a><span data-ttu-id="98746-230">ライフサイクル</span><span class="sxs-lookup"><span data-stu-id="98746-230">Lifecycle</span></span>

<span data-ttu-id="98746-231">編集可能な ER コンポーネントのラベルは、ER コンフィギュレーションの適切なバージョンで、コンポーネントのその他のコンテンツと共に保持されます。</span><span class="sxs-lookup"><span data-stu-id="98746-231">Labels of an ER component that can be edited are kept, together with other content for the component, in the appropriate version of an ER configuration.</span></span>

<span data-ttu-id="98746-232">ベースとなる ER コンポーネントのラベルは、変更を加えるために作成する ER コンポーネントの派生バージョンで参照できます。</span><span class="sxs-lookup"><span data-stu-id="98746-232">Labels of a base ER component can be referred to in a derived version of the ER component that you create to introduce your modifications.</span></span>

<span data-ttu-id="98746-233">ER バージョン管理では、ER コンポーネント内の任意の属性に対するラベル割り当てを制御します。</span><span class="sxs-lookup"><span data-stu-id="98746-233">ER versioning controls label assignment to any attribute in an ER component.</span></span> <span data-ttu-id="98746-234">ラベルの割り当てに対する変更は、提供された ER コンポーネントの派生バージョンとして作成された編集可能な ER コンポーネントの変更 (デルタ) の一覧に記録されます。</span><span class="sxs-lookup"><span data-stu-id="98746-234">Changes to the label assignment are recorded in the list of changes (delta) of an editable ER component that has been created as a derived version of the provided ER component.</span></span> <span data-ttu-id="98746-235">これらの変更は、派生バージョンが新しいベース バージョンに再ベースされるときに検証されます。</span><span class="sxs-lookup"><span data-stu-id="98746-235">These changes will be validated when a derived version is rebased to a new base version.</span></span>

## <a name="functions"></a><span data-ttu-id="98746-236">関数</span><span class="sxs-lookup"><span data-stu-id="98746-236">Functions</span></span>

<span data-ttu-id="98746-237">組み込みの [LISTOFFIELDS](er-functions-list-listoffields.md) ER 関数を使用すると、ER コンポーネントの一部の項目に対して構成されている ER ラベルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="98746-237">The built-in [LISTOFFIELDS](er-functions-list-listoffields.md) ER function can access ER labels that have been configured for some items of ER components.</span></span>

<span data-ttu-id="98746-238">このトピックで既に説明したように、すべての [モデル](#LinkModelEnum) または [形式](#LinkFormatEnum) ER 列挙値の **ラベル** および **説明** 属性は、適切な ER コンポーネントでアクセスできる ER ラベルにリンクできます。</span><span class="sxs-lookup"><span data-stu-id="98746-238">As described earlier in this topic, the **Label** and **Description** attributes of every [model](#LinkModelEnum) or [format](#LinkFormatEnum) ER enumeration's value can be linked to an ER label that is accessible in the appropriate ER component.</span></span> <span data-ttu-id="98746-239">引数として ER 列挙を使用すると、**LISTOFFIELDS** 関数を呼び出す ER 式を構成できます。</span><span class="sxs-lookup"><span data-stu-id="98746-239">You can configure an ER expression where you call the **LISTOFFIELDS** function by using the ER enumeration as an argument.</span></span> <span data-ttu-id="98746-240">この式は、この関数の引数として定義されている ER 列挙のすべての値のレコードを含むリストを返します。</span><span class="sxs-lookup"><span data-stu-id="98746-240">This expression returns a list that contains a record for every value of an ER enumeration that has been defined as an argument of this function.</span></span> <span data-ttu-id="98746-241">各レコードには ER 列挙値にリンクされた ER ラベルの値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="98746-241">Every record contains the value of an ER label that is linked to an ER enumeration value:</span></span>

- <span data-ttu-id="98746-242">**ラベル** 属性にリンクされている ER ラベルの値は、返された レコードの **ラベル** フィールドに格納されます。</span><span class="sxs-lookup"><span data-stu-id="98746-242">The value of an ER label that is linked to the **Label** attributes is stored in the **Label** field of the returned record.</span></span>
- <span data-ttu-id="98746-243">**説明** 属性にリンクされている ER ラベルの値は、返された レコードの **説明** フィールドに格納されます。</span><span class="sxs-lookup"><span data-stu-id="98746-243">The value of an ER label that is linked to the **Description** attributes is stored in the **Description** field of the returned record.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98746-244">追加リソース</span><span class="sxs-lookup"><span data-stu-id="98746-244">Additional resources</span></span>

- [<span data-ttu-id="98746-245">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="98746-245">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="98746-246">電子申告機能</span><span class="sxs-lookup"><span data-stu-id="98746-246">Electronic Reporting functions</span></span>](er-formula-language.md#functions)
