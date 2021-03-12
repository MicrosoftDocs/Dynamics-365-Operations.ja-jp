---
title: 構成済み ER コンポーネントを検査して、ランタイムの問題を回避する
description: このトピックでは、構成済み電子レポート (ER) コンポーネントを検査して、発生する可能性のあるランタイムの問題を回避する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ba696fb7a8d9083d11cc29953cf1340a581afcf
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797344"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a><span data-ttu-id="f526d-103">構成済み ER コンポーネントを検査して、ランタイムの問題を回避する</span><span class="sxs-lookup"><span data-stu-id="f526d-103">Inspect the configured ER component to prevent runtime issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f526d-104">すべての構成済み [電子レポート (ER)](general-electronic-reporting.md) [形式](general-electronic-reporting.md#FormatComponentOutbound) と [モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components) コンポーネントは、設計時に [検証](er-fillable-excel.md#validate-an-er-format) できます。</span><span class="sxs-lookup"><span data-stu-id="f526d-104">Every configured [Electronic reporting (ER)](general-electronic-reporting.md) [format](general-electronic-reporting.md#FormatComponentOutbound) and [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component can be [validated](er-fillable-excel.md#validate-an-er-format) at design time.</span></span> <span data-ttu-id="f526d-105">この検証では、実行エラーやパフォーマンスの低下など、発生する可能性のあるランタイムの問題を防ぐために、整合性チェックが実行されます。</span><span class="sxs-lookup"><span data-stu-id="f526d-105">During this validation, a consistency check runs to help prevent runtime issues that might occur, such as execution errors and performance degradation.</span></span> <span data-ttu-id="f526d-106">このチェックでは、検出された問題ごとに、問題のある要素のパスを提供します。</span><span class="sxs-lookup"><span data-stu-id="f526d-106">For every issue found, the check provides the path of a problematic element.</span></span> <span data-ttu-id="f526d-107">一部の問題については、自動修正が利用できます。</span><span class="sxs-lookup"><span data-stu-id="f526d-107">For some issues, an automatic fix is available.</span></span>

<span data-ttu-id="f526d-108">既定では、前述の ER コンポーネントを含む ER 構成について、次の場合に検証が自動的に適用されます:</span><span class="sxs-lookup"><span data-stu-id="f526d-108">By default, the validation is automatically applied in the following cases for an ER configuration that contains the previously mentioned ER components:</span></span>

- <span data-ttu-id="f526d-109">ER 構成の新しい [バージョン](general-electronic-reporting.md#component-versioning) を Microsoft Dynamics 365 Finance のインスタンスに [インポート](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) します。</span><span class="sxs-lookup"><span data-stu-id="f526d-109">You [import](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) a new [version](general-electronic-reporting.md#component-versioning) of an ER configuration into your instance of Microsoft Dynamics 365 Finance.</span></span>
- <span data-ttu-id="f526d-110">編集可能な ER 構成の [状態](general-electronic-reporting.md#component-versioning) を **ドラフト** から **完了** に変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-110">You change the [status](general-electronic-reporting.md#component-versioning) of the editable ER configuration from **Draft** to **Completed**.</span></span>
- <span data-ttu-id="f526d-111">新しい基本バージョンを適用することにより、編集可能な ER 構成を [リベース](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) します。</span><span class="sxs-lookup"><span data-stu-id="f526d-111">You [rebase](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) an editable ER configuration by applying a new base version.</span></span>

<span data-ttu-id="f526d-112">この検証を明示的に実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="f526d-112">You can explicitly run this validation.</span></span> <span data-ttu-id="f526d-113">次の 3 つのオプションのいずれかを選択し、指定されている手順に従います:</span><span class="sxs-lookup"><span data-stu-id="f526d-113">Select one of the following three options, and follow the steps that are provided:</span></span>

- <span data-ttu-id="f526d-114">オプション 1:</span><span class="sxs-lookup"><span data-stu-id="f526d-114">Option 1:</span></span>

    1. <span data-ttu-id="f526d-115">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f526d-115">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="f526d-116">左側のペインにある構成ツリーで、ER 形式または ER モデル マッピング コンポーネントを含む目的の ER 構成を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-116">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format or ER model mapping component.</span></span>
    3. <span data-ttu-id="f526d-117">**バージョン** クイック タブで、選択した ER 構成の目的のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-117">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="f526d-118">アクション ペインで、**検証** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-118">On the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="f526d-119">オプション 2、ER 形式の場合:</span><span class="sxs-lookup"><span data-stu-id="f526d-119">Option 2, for an ER format:</span></span>

    1. <span data-ttu-id="f526d-120">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f526d-120">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="f526d-121">左側のペインにある構成ツリーで、ER 形式のコンポーネントを含む目的の ER 構成を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-121">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format component.</span></span>
    3. <span data-ttu-id="f526d-122">**バージョン** クイック タブで、選択した ER 構成の目的のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-122">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="f526d-123">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-123">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="f526d-124">**形式デザイナー** ページのアクション ペインで、**検証** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-124">On the **Format designer** page, on the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="f526d-125">オプション 3、ER モデル マッピングの場合:</span><span class="sxs-lookup"><span data-stu-id="f526d-125">Option 3, for an ER model mapping:</span></span>

    1. <span data-ttu-id="f526d-126">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f526d-126">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="f526d-127">左側のペインにある構成ツリーで、ER モデル マッピング コンポーネントを含む目的の ER 構成を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-127">In the configurations tree in the left pane, select the desired ER configuration that contains the ER model mapping component.</span></span>
    3. <span data-ttu-id="f526d-128">**バージョン** クイック タブで、選択した ER 構成の目的のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-128">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="f526d-129">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-129">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="f526d-130">**モデルからデータ ソースへのマッピング** ページのアクション ペインで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-130">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>
    6. <span data-ttu-id="f526d-131">**モデル マッピング デザイナー** ページのアクション ペインで、**検証** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-131">On the **Model mapping designer** page, on the Action Pane, select **Validate**.</span></span>

<span data-ttu-id="f526d-132">構成のインポート時に、検証をスキップするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f526d-132">To skip the validation when the configuration is imported, follow these steps.</span></span>

1. <span data-ttu-id="f526d-133">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f526d-133">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f526d-134">**構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-134">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="f526d-135">**インポート後に構成を検証** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-135">Set the **Validate the configuration after importing** option to **No**.</span></span>

<span data-ttu-id="f526d-136">バージョンの状態を変更またはリベースするときに検証をスキップするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f526d-136">To skip the validation when you change or rebase the version's status, follow these steps.</span></span>

1. <span data-ttu-id="f526d-137">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f526d-137">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f526d-138">**構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-138">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="f526d-139">**構成状態の変更時およびリベース時に検証をスキップ** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-139">Set the **Skip validation at configuration's status change and rebase** option to **Yes**.</span></span>

<span data-ttu-id="f526d-140">ER では、次のカテゴリを使用して、整合性チェック検査をグループ化します:</span><span class="sxs-lookup"><span data-stu-id="f526d-140">ER uses the following categories to group consistency check inspections:</span></span>

- <span data-ttu-id="f526d-141">**実行可能性** – 実行時に発生する可能性がある重大な問題を検出する検査。</span><span class="sxs-lookup"><span data-stu-id="f526d-141">**Executability** – Inspections that detect critical issues that might happen at runtime.</span></span> <span data-ttu-id="f526d-142">これらの問題は、ほとんどが **エラー** レベルです。</span><span class="sxs-lookup"><span data-stu-id="f526d-142">These issues are mostly at an **Error** level.</span></span> 
- <span data-ttu-id="f526d-143">**パフォーマンス** – 構成済み ER コンポーネントの非効率な実行を引き起こす可能性のある問題を検出する検査。</span><span class="sxs-lookup"><span data-stu-id="f526d-143">**Performance** – Inspections that detect issues that might cause inefficient execution of configured ER components.</span></span> <span data-ttu-id="f526d-144">これらの問題は、ほとんどが **警告** レベルです。</span><span class="sxs-lookup"><span data-stu-id="f526d-144">These issues are mostly at a **Warning** level.</span></span>
- <span data-ttu-id="f526d-145">**データの整合性** – データ損失または実行時の問題を引き起こす可能性のある問題を検出する検査。</span><span class="sxs-lookup"><span data-stu-id="f526d-145">**Data integrity** – Inspections that detect issues that might cause data loss or runtime issues.</span></span> <span data-ttu-id="f526d-146">これらの問題は、ほとんどが **警告** レベルです。</span><span class="sxs-lookup"><span data-stu-id="f526d-146">These issues are mostly at a **Warning** level.</span></span>

## <a name="list-of-inspections"></a><span data-ttu-id="f526d-147">検査の一覧</span><span class="sxs-lookup"><span data-stu-id="f526d-147">List of inspections</span></span>

<span data-ttu-id="f526d-148">次の表は、ER が提供する検査の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="f526d-148">The following table provides an overview of the inspections that ER provides.</span></span> <span data-ttu-id="f526d-149">これらの検査の詳細については、最初の列のリンクを使用して、このトピックの関連するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-149">For more information about these inspections, use the links in the first column to go to the relevant sections of this topic.</span></span> <span data-ttu-id="f526d-150">これらのセクションでは、ER が検査を提供するコンポーネントのタイプと、問題を防ぐために ER コンポーネントを再構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f526d-150">Those sections explain the types of components that ER provides inspections for and how you can reconfigure ER components to help prevent issues.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f526d-151">氏名</span><span class="sxs-lookup"><span data-stu-id="f526d-151">Name</span></span></th>
<th><span data-ttu-id="f526d-152">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="f526d-152">Category</span></span></th>
<th><span data-ttu-id="f526d-153">レベル</span><span class="sxs-lookup"><span data-stu-id="f526d-153">Level</span></span></th>
<th><span data-ttu-id="f526d-154">メッセージ</span><span class="sxs-lookup"><span data-stu-id="f526d-154">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f526d-155"><a href='#i1'>型変換</a></span><span class="sxs-lookup"><span data-stu-id="f526d-155"><a href='#i1'>Type conversion</a></span></span></td>
<td><span data-ttu-id="f526d-156">実行可能性</span><span class="sxs-lookup"><span data-stu-id="f526d-156">Executability</span></span></td>
<td><span data-ttu-id="f526d-157">エラー</span><span class="sxs-lookup"><span data-stu-id="f526d-157">Error</span></span></td>
<td>
<p><span data-ttu-id="f526d-158">タイプ &lt;type&gt; の式をタイプ &lt;type&gt; のフィールドに変換できません。</span><span class="sxs-lookup"><span data-stu-id="f526d-158">Cannot convert expression of type &lt;type&gt; to field of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="f526d-159"><b>ランタイム エラー:</b> タイプの例外</span><span class="sxs-lookup"><span data-stu-id="f526d-159"><b>Runtime error:</b> Exception for type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="f526d-160"><a href='#i2'>タイプの互換性</a></span><span class="sxs-lookup"><span data-stu-id="f526d-160"><a href='#i2'>Type compatibility</a></span></span></td>
<td><span data-ttu-id="f526d-161">実行可能性</span><span class="sxs-lookup"><span data-stu-id="f526d-161">Executability</span></span></td>
<td><span data-ttu-id="f526d-162">エラー</span><span class="sxs-lookup"><span data-stu-id="f526d-162">Error</span></span></td>
<td>
<p><span data-ttu-id="f526d-163">構成済みの式は、現在の形式要素をデータ ソースにバインドするために使用できません。この式が、現在の形式要素のタイプ &lt;type&gt; でサポートされているデータ型の範囲を超えたデータ型 &lt;type&gt; の値を返すためです。</span><span class="sxs-lookup"><span data-stu-id="f526d-163">The configured expression cannot be used as the binding of the current format element to a data source as this expression returns value of the data type &lt;type&gt; that is beyond the scope of data types that are supported by the current format element of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="f526d-164"><b>ランタイム エラー:</b> タイプの例外</span><span class="sxs-lookup"><span data-stu-id="f526d-164"><b>Runtime error:</b> Exception of type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="f526d-165"><a href='#i3'>構成要素の欠落</a></span><span class="sxs-lookup"><span data-stu-id="f526d-165"><a href='#i3'>Missing configuration element</a></span></span></td>
<td><span data-ttu-id="f526d-166">実行可能性</span><span class="sxs-lookup"><span data-stu-id="f526d-166">Executability</span></span></td>
<td><span data-ttu-id="f526d-167">エラー</span><span class="sxs-lookup"><span data-stu-id="f526d-167">Error</span></span></td>
<td>
<p><span data-ttu-id="f526d-168">パスが見つかりません &lt;path&gt;。</span><span class="sxs-lookup"><span data-stu-id="f526d-168">Path not found &lt;path&gt;.</span></span></p>
<p><span data-ttu-id="f526d-169"><b>ランタイム エラー:</b> 構成要素 &lt;path&gt; が見つかりません</span><span class="sxs-lookup"><span data-stu-id="f526d-169"><b>Runtime error:</b> Element of the configuration &lt;path&gt; not found</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="f526d-170"><a href='#i4'>FILTER 関数による式の実行可能性</a></span><span class="sxs-lookup"><span data-stu-id="f526d-170"><a href='#i4'>Executability of an expression with FILTER function</a></span></span></td>
<td><span data-ttu-id="f526d-171">実行可能性</span><span class="sxs-lookup"><span data-stu-id="f526d-171">Executability</span></span></td>
<td><span data-ttu-id="f526d-172">エラー</span><span class="sxs-lookup"><span data-stu-id="f526d-172">Error</span></span></td>
<td>
<p><span data-ttu-id="f526d-173">FILTER 関数のリスト式がクエリ可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="f526d-173">The list expression of FILTER function is not queryable.</span></span></p>
<p><span data-ttu-id="f526d-174"><b>ランタイム エラー:</b> フィルター処理はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f526d-174"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="f526d-175">構成を検証して、詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="f526d-175">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="f526d-176"><a href='#i5'>GROUPBY データ ソースの実行可能性</a></span><span class="sxs-lookup"><span data-stu-id="f526d-176"><a href='#i5'>Executability of a GROUPBY data source</a></span></span></td>
<td><span data-ttu-id="f526d-177">実行可能性</span><span class="sxs-lookup"><span data-stu-id="f526d-177">Executability</span></span></td>
<td><span data-ttu-id="f526d-178">エラー</span><span class="sxs-lookup"><span data-stu-id="f526d-178">Error</span></span></td>
<td><span data-ttu-id="f526d-179">パス &lt;path&gt; は、クエリをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="f526d-179">Path &lt;path&gt; does not support querying.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f526d-180">実行可能性</span><span class="sxs-lookup"><span data-stu-id="f526d-180">Executability</span></span></td>
<td><span data-ttu-id="f526d-181">エラー</span><span class="sxs-lookup"><span data-stu-id="f526d-181">Error</span></span></td>
<td>
<p><span data-ttu-id="f526d-182">Group by 関数はクエリで実行できません。</span><span class="sxs-lookup"><span data-stu-id="f526d-182">Group by function cannot be executed with query.</span></span></p>
<p><span data-ttu-id="f526d-183"><b>ランタイム エラー:</b> Group by 関数はクエリで実行できません。</span><span class="sxs-lookup"><span data-stu-id="f526d-183"><b>Runtime error:</b> Group by function can't be executed with query.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="f526d-184"><a href='#i6'>JOIN データ ソースの実行可能性</a></span><span class="sxs-lookup"><span data-stu-id="f526d-184"><a href='#i6'>Executability of a JOIN data source</a></span></span></td>
<td><span data-ttu-id="f526d-185">実行可能性</span><span class="sxs-lookup"><span data-stu-id="f526d-185">Executability</span></span></td>
<td><span data-ttu-id="f526d-186">エラー</span><span class="sxs-lookup"><span data-stu-id="f526d-186">Error</span></span></td>
<td>
<p><span data-ttu-id="f526d-187">クエリのフィルターではないリスト &lt;path&gt; を結合できません。</span><span class="sxs-lookup"><span data-stu-id="f526d-187">Cannot join a list &lt;path&gt; that is not a filter in query.</span></span></p>
<p><span data-ttu-id="f526d-188"><b>ランタイム エラー:</b> 関数結合された datasource は、計算済フィールドが正しく呼び出されていないフィルター式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f526d-188"><b>Runtime error:</b> Function Joined datasource should be a filter expression calculated field has been incorrectly called.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="f526d-189"><a href='#i7'>FILTER 関数 対 WHERE 関数の優先度</a></span><span class="sxs-lookup"><span data-stu-id="f526d-189"><a href='#i7'>Preferability of FILTER vs WHERE function</a></span></span></td>
<td><span data-ttu-id="f526d-190">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="f526d-190">Performance</span></span></td>
<td><span data-ttu-id="f526d-191">警告</span><span class="sxs-lookup"><span data-stu-id="f526d-191">Warning</span></span></td>
<td><span data-ttu-id="f526d-192">パフォーマンスの観点から、式には WHERE 関数よりも FILTER 関数を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f526d-192">Using FILTER function for the expression is preferable than WHERE from the performance perspective.</span></span> <span data-ttu-id="f526d-193">[修正] を選択すると、自動的に置換します。</span><span class="sxs-lookup"><span data-stu-id="f526d-193">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f526d-194"><a href='#i8'>ALLITEMSQUERY 関数 対 ALLITEMS 関数の優先度</a></span><span class="sxs-lookup"><span data-stu-id="f526d-194"><a href='#i8'>Preferability of ALLITEMSQUERY vs ALLITEMS function</a></span></span></td>
<td><span data-ttu-id="f526d-195">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="f526d-195">Performance</span></span></td>
<td><span data-ttu-id="f526d-196">警告</span><span class="sxs-lookup"><span data-stu-id="f526d-196">Warning</span></span></td>
<td><span data-ttu-id="f526d-197">パフォーマンスの観点から、式には ALLITEMS 関数よりも ALLITEMSQUERY 関数を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f526d-197">Using ALLITEMSQUERY function for the expression is preferable than ALLITEMS from the performance perspective.</span></span> <span data-ttu-id="f526d-198">[修正] を選択すると、自動的に置換します。</span><span class="sxs-lookup"><span data-stu-id="f526d-198">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f526d-199"><a href='#i9'>空リストの場合の考慮</a></span><span class="sxs-lookup"><span data-stu-id="f526d-199"><a href='#i9'>Consideration of empty list cases</a></span></span></td>
<td><span data-ttu-id="f526d-200">実行可能性</span><span class="sxs-lookup"><span data-stu-id="f526d-200">Executability</span></span></td>
<td><span data-ttu-id="f526d-201">警告</span><span class="sxs-lookup"><span data-stu-id="f526d-201">Warning</span></span></td>
<td>
<p><span data-ttu-id="f526d-202">リスト &lt;パス&gt; に空リストの場合のチェックがなく、実行時にエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f526d-202">List &lt;path&gt; does not have any check for empty list case, it can result an error at run time.</span></span> <span data-ttu-id="f526d-203">空リストの場合のチェックを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-203">Add a check for empty list case.</span></span></p>
<p><span data-ttu-id="f526d-204"><b>ランタイム エラー:</b> リストは &lt;path&gt; で空です</span><span class="sxs-lookup"><span data-stu-id="f526d-204"><b>Runtime error:</b> List is empty at &lt;path&gt;</span></span></p>
<p><span data-ttu-id="f526d-205"><b><a href='#i9a'>潜在的な問題</a>:</b> 入力元のデータ ソースに複数のレコードが含まれているときに、行が 1 回入力されます</span><span class="sxs-lookup"><span data-stu-id="f526d-205"><b><a href='#i9a'>Potential issue</a>:</b> Line is getting populated once while a data source it is populated from contains multiple records</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="f526d-206"><a href='#i10'>FILTER 関数による式の実行可能性 (キャッシュ)</a></span><span class="sxs-lookup"><span data-stu-id="f526d-206"><a href='#i10'>Executability of an expression with FILTER function (caching)</a></span></span></td>
<td><span data-ttu-id="f526d-207">実行可能性</span><span class="sxs-lookup"><span data-stu-id="f526d-207">Executability</span></span></td>
<td><span data-ttu-id="f526d-208">エラー</span><span class="sxs-lookup"><span data-stu-id="f526d-208">Error</span></span></td>
<td>
<p><span data-ttu-id="f526d-209">FILTER 関数を、選択したデータ ソースのタイプに適用することはできません。</span><span class="sxs-lookup"><span data-stu-id="f526d-209">FILTER function cannot be applied to the selected type of data source.</span></span> <span data-ttu-id="f526d-210">テーブル レコード タイプのデータ ソースは、キャッシュされておらず、入れ子にされたデータ ソースが手動で追加されていない場合にのみ適用できます。</span><span class="sxs-lookup"><span data-stu-id="f526d-210">A data source of the Table records type is applicable only when it is not cached and has no manually added nested data sources.</span></span></p>
<p><span data-ttu-id="f526d-211"><b>ランタイム エラー:</b> フィルター処理はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f526d-211"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="f526d-212">構成を検証して、詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="f526d-212">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="f526d-213"><a href='#i11'>バインドの欠落</a></span><span class="sxs-lookup"><span data-stu-id="f526d-213"><a href='#i11'>Missing binding</a></span></span></td>
<td><span data-ttu-id="f526d-214">実行可能性</span><span class="sxs-lookup"><span data-stu-id="f526d-214">Executability</span></span></td>
<td><span data-ttu-id="f526d-215">警告</span><span class="sxs-lookup"><span data-stu-id="f526d-215">Warning</span></span></td>
<td>
<p><span data-ttu-id="f526d-216">パス &lt;path&gt; は、モデルのマッピングを使用しているどの datasource にもバインドされません。</span><span class="sxs-lookup"><span data-stu-id="f526d-216">Path &lt;path&gt; has no binding to any datasource in using model's mapping.</span></span></p>
<p><span data-ttu-id="f526d-217"><b>ランタイム エラー:</b> パス &lt;path&gt; がバインドされていません</span><span class="sxs-lookup"><span data-stu-id="f526d-217"><b>Runtime error:</b> Path &lt;path&gt; is not bound</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="f526d-218"><a href='#i12'>リンクされていないテンプレート</a></span><span class="sxs-lookup"><span data-stu-id="f526d-218"><a href='#i12'>Not linked template</a></span></span></td>
<td><span data-ttu-id="f526d-219">データの整合性</span><span class="sxs-lookup"><span data-stu-id="f526d-219">Data integrity</span></span></td>
<td><span data-ttu-id="f526d-220">警告</span><span class="sxs-lookup"><span data-stu-id="f526d-220">Warning</span></span></td>
<td><span data-ttu-id="f526d-221">ファイル &lt;name&gt; はファイル コンポーネントにリンクされておらず、構成バージョンの状態の変更後に削除されます。</span><span class="sxs-lookup"><span data-stu-id="f526d-221">File &lt;name&gt; is linked to no file components and will be removed after changing status of configuration version.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f526d-222"><a href='#i13'>未同期形式</a></span><span class="sxs-lookup"><span data-stu-id="f526d-222"><a href='#i13'>Not synced format</a></span></span></td>
<td><span data-ttu-id="f526d-223">データの整合性</span><span class="sxs-lookup"><span data-stu-id="f526d-223">Data integrity</span></span></td>
<td><span data-ttu-id="f526d-224">警告</span><span class="sxs-lookup"><span data-stu-id="f526d-224">Warning</span></span></td>
<td><span data-ttu-id="f526d-225">定義名 &lt;component name&gt; は Excel シート &lt;sheet name&gt; には存在しません</span><span class="sxs-lookup"><span data-stu-id="f526d-225">Defined name &lt;component name&gt; does not exist in Excel sheet &lt;sheet name&gt;</span></span></td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a><span data-ttu-id="f526d-226">型変換</span><span class="sxs-lookup"><span data-stu-id="f526d-226">Type conversion</span></span>

<span data-ttu-id="f526d-227">ER では、データ モデル フィールドのデータ型が、そのフィールドのバインドとして構成されている式のデータ型と互換性があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-227">ER checks whether the data type of a data model field is compatible with the data type of an expression that is configured as the binding of that field.</span></span> <span data-ttu-id="f526d-228">データ型に互換性がない場合は、ER モデル マッピング デザイナーで検証エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f526d-228">If the data types are incompatible, a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="f526d-229">受信するメッセージは、ER がタイプ A の式をタイプ B のフィールドに変換できないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-229">The message that you receive states that ER can't convert an expression of type A to a field of type B.</span></span>

<span data-ttu-id="f526d-230">次の手順は、この問題がどのように発生するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-230">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="f526d-231">ER データ モデルと ER モデル マッピング コンポーネントの構成を同時に開始します。</span><span class="sxs-lookup"><span data-stu-id="f526d-231">Start to configure the ER data model and the ER model-mapping components simultaneously.</span></span>
2. <span data-ttu-id="f526d-232">データ モデル ツリーで、**X** という名前のフィールドを追加 し、データ型として **整数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-232">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![データ モデル ページのデータ モード ツリーに追加された X フィールドおよび整数データ型](./media/er-components-inspections-01.png)

3. <span data-ttu-id="f526d-234">モデル マッピング データ ソース ペインで、**計算済フィールド** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-234">In the model-mapping data sources pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="f526d-235">新しいデータソースに **Y** と名前を付けて、式 `INTVALUE(100)` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-235">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="f526d-236">**X** を **Y** にバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-236">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="f526d-237">データ モデル デザイナーで、**X** フィールドのデータ型を **整数** から **Int64** に変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-237">In the data model designer, change the data type of the **X** field from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="f526d-238">**検証** を選択して、**モデル マッピング デザイナー** ページで編集可能なモデル マッピング コンポーネントを検査します。</span><span class="sxs-lookup"><span data-stu-id="f526d-238">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![モデル マッピング デザイナー ページで編集可能なモデル マッピング コンポーネントを検証する](./media/er-components-inspections-01.gif)

8. <span data-ttu-id="f526d-240">**検証** を選択して、**構成** ページで選択した ER 構成のモデル マッピング コンポーネントを検査します。</span><span class="sxs-lookup"><span data-stu-id="f526d-240">Select **Validate** to inspect the model-mapping component of the selected ER configuration on the **Configurations** page.</span></span>

    ![検証して、構成ページでモデル マッピング コンポーネントを検査します](./media/er-components-inspections-01a.png)

9. <span data-ttu-id="f526d-242">検証エラーが発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-242">Notice that a validation error occurs.</span></span> <span data-ttu-id="f526d-243">このメッセージは、**Y** データ ソースの `INTVALUE(100)` 式が返す **整数** タイプの値を、**Int64** タイプの **X** データ モデル フィールドに格納できないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-243">The message states that the value of the **Integer** type that the `INTVALUE(100)` expression of the **Y** data source returns can't be stored in the **X** data model field of the **Int64** type.</span></span>

<span data-ttu-id="f526d-244">次の図は、警告を無視し、**実行** を選択して、モデル マッピングを使用するように構成された形式を実行した場合に発生するランタイム エラーを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-244">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model-mapping.</span></span>

![フォーマット デザイナー ページのランタイム エラー](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="f526d-246">自動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-246">Automatic resolution</span></span>

<span data-ttu-id="f526d-247">この問題を自動的に修正するオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="f526d-247">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="f526d-248">手動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-248">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="f526d-249">オプション 1</span><span class="sxs-lookup"><span data-stu-id="f526d-249">Option 1</span></span>

<span data-ttu-id="f526d-250">データ モデル フィールドのデータ型を変更して、そのフィールドのバインドに対して構成された式のデータ型と一致するように、データ モデルの構造を更新します。</span><span class="sxs-lookup"><span data-stu-id="f526d-250">Update the data model structure by changing the data type of the data model field so that it matches the data type of the expression that is configured for the binding of that field.</span></span> <span data-ttu-id="f526d-251">前の例では、**X** フィールドのデータ型を **整数** に戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f526d-251">For the preceding example, the data type of the **X** field must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="f526d-252">オプション 2</span><span class="sxs-lookup"><span data-stu-id="f526d-252">Option 2</span></span>

<span data-ttu-id="f526d-253">データ モデル フィールドに関連付けられたデータ ソースの式を変更することにより、モデル マッピングを更新します。</span><span class="sxs-lookup"><span data-stu-id="f526d-253">Update the model-mapping by changing the expression of the data source that is bound with the data model field.</span></span> <span data-ttu-id="f526d-254">前の例では、**Y** データ ソースの式を `INT64VALUE(100)` に変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f526d-254">For the preceding example, the expression of the **Y** data source must be changed to `INT64VALUE(100)`.</span></span>

## <a name="type-compatibility"></a><a id="i2"></a><span data-ttu-id="f526d-255">タイプの互換性</span><span class="sxs-lookup"><span data-stu-id="f526d-255">Type compatibility</span></span>

<span data-ttu-id="f526d-256">ER では、形式要素のデータ型が、その形式要素のバインドとして構成されている式のデータ型と互換性があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-256">ER checks whether the data type of a format element is compatible with the data type of an expression that is configured as the binding of that format element.</span></span> <span data-ttu-id="f526d-257">データ型に互換性がない場合は、ER 操作デザイナーで検証エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f526d-257">If the data types are incompatible, a validation error occurs in the ER Operations designer.</span></span> <span data-ttu-id="f526d-258">受信するメッセージは、構成済みの式が現在の形式要素をデータ ソースにバインドするために使用できないことを示しています。これは、式が、現在の形式要素のタイプ Bでサポートされているデータ型の範囲を超えるデータ型 A の値を返すためです。</span><span class="sxs-lookup"><span data-stu-id="f526d-258">The message that you receive states that the configured expression can't be used as the binding of the current format element to a data source, because the expression returns a value of data type A that is beyond the scope of the data types that are supported by the current format element of type B.</span></span>

<span data-ttu-id="f526d-259">次の手順は、この問題がどのように発生するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-259">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="f526d-260">ER データ モデルと ER 形式コンポーネントの構成を同時に開始します。</span><span class="sxs-lookup"><span data-stu-id="f526d-260">Start to configure the ER data model and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="f526d-261">データ モデル ツリーで、**X** という名前のフィールドを追加 し、データ型として **整数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-261">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>
3. <span data-ttu-id="f526d-262">形式構造ツリーで、**数値** タイプの形式要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-262">In the format structure tree, add a format element of the **Numeric** type.</span></span>
4. <span data-ttu-id="f526d-263">新しい形式要素 **Y** に名前を付けます。**数値タイプ** フィールドで、データ型として **整数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-263">Name the new format element **Y**. In the **Numeric type** field, select **Integer** as the data type.</span></span>
5. <span data-ttu-id="f526d-264">**X** を **Y** にバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-264">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="f526d-265">形式構造ツリーで、**Y** 形式要素のデータ型を **整数** から **Int64** に変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-265">In the format structure tree, change the data type of the **Y** format element from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="f526d-266">**検証** を選択して、**形式デザイナー** ページで編集可能な形式コンポーネントを検査します。</span><span class="sxs-lookup"><span data-stu-id="f526d-266">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![形式デザイナー ページでタイプの互換性を検証する](./media/er-components-inspections-02.gif)

8. <span data-ttu-id="f526d-268">検証エラーが発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-268">Notice that a validation error occurs.</span></span> <span data-ttu-id="f526d-269">メッセージは、構成済みの式が **Int64** 値のみを受け入れることができることを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-269">The message states that the configured expression can accept only **Int64** values.</span></span> <span data-ttu-id="f526d-270">したがって、**整数** タイプの **X** データ モデル フィールドの値を **Y** 形式要素に入力することはできません。</span><span class="sxs-lookup"><span data-stu-id="f526d-270">Therefore, the value of the **X** data model field of the **Integer** type can't be entered in the **Y** format element.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="f526d-271">自動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-271">Automatic resolution</span></span>

<span data-ttu-id="f526d-272">この問題を自動的に修正するオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="f526d-272">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="f526d-273">手動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-273">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="f526d-274">オプション 1</span><span class="sxs-lookup"><span data-stu-id="f526d-274">Option 1</span></span>

<span data-ttu-id="f526d-275">**数値** 形式要素のデータ型を変更して、その要素のバインドに対して構成された式のデータ型と一致するように、形式構造を更新します。</span><span class="sxs-lookup"><span data-stu-id="f526d-275">Update the format structure by changing the data type of the **Numeric** format element so that it matches the data type of the expression that you configured for the binding of that element.</span></span> <span data-ttu-id="f526d-276">前の例では、**X** 形式要素の **数値タイプ** の値を **整数** に戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f526d-276">In the preceding example, the **Numeric type** value of the **X** format element must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="f526d-277">オプション 2</span><span class="sxs-lookup"><span data-stu-id="f526d-277">Option 2</span></span>

<span data-ttu-id="f526d-278">`model.X` から `INT64VALUE(model.X)` に式をに変更して、**X** 形式要素の形式マッピングを更新します。</span><span class="sxs-lookup"><span data-stu-id="f526d-278">Update the format mapping of the **X** format element by changing the expression from `model.X` to `INT64VALUE(model.X)`.</span></span>

## <a name="missing-configuration-element"></a><a id="i3"></a><span data-ttu-id="f526d-279">構成要素の欠落</span><span class="sxs-lookup"><span data-stu-id="f526d-279">Missing configuration element</span></span>

<span data-ttu-id="f526d-280">ER は、編集可能な ER コンポーネントで構成されているデータソースだけがバインド式に含まれているかどうかをを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-280">ER checks whether the binding expressions contain only data sources that are configured in the editable ER component.</span></span> <span data-ttu-id="f526d-281">編集可能な ER コンポーネントに存在しないデータ ソースを含むすべてのバインドで、ER 操作デザイナーまたは ER モデル マッピング デザイナーで検証エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f526d-281">For every binding that contains a data source that is missing in the editable ER component, a validation error occurs in the ER Operations designer or the ER model-mapping designer.</span></span>

<span data-ttu-id="f526d-282">次の手順は、この問題がどのように発生するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-282">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="f526d-283">ER データ モデルと ER モデル マッピング コンポーネントの構成を同時に開始します。</span><span class="sxs-lookup"><span data-stu-id="f526d-283">Start to configure the ER data model and the ER model-mapping components simultaneously.</span></span>
2. <span data-ttu-id="f526d-284">データ モデル ツリーで、**X** という名前のフィールドを追加 し、データ型として **整数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-284">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![データ モデル ページに X フィールドと整数データ型があるデータ モード ツリー](./media/er-components-inspections-01.png)

3. <span data-ttu-id="f526d-286">モデル マッピング データ ソース ペインで、**計算済フィールド** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-286">In the model-mapping data sources pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="f526d-287">新しいデータソースに **Y** と名前を付けて、式 `INTVALUE(100)` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-287">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="f526d-288">**X** を **Y** にバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-288">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="f526d-289">モデル マッピング デザイナーのデータ ソース ペインで、**Y** データ ソースを削除します。</span><span class="sxs-lookup"><span data-stu-id="f526d-289">In the model-mapping designer, in the data sources pane, delete the **Y** data source.</span></span>
7. <span data-ttu-id="f526d-290">**検証** を選択して、**モデル マッピング デザイナー** ページで編集可能なモデル マッピング コンポーネントを検査します。</span><span class="sxs-lookup"><span data-stu-id="f526d-290">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![モデル マッピング デザイナー ページで編集可能な ER モデル マッピング コンポーネントを検査する](./media/er-components-inspections-03.gif)

8. <span data-ttu-id="f526d-292">検証エラーが発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-292">Notice that a validation error occurs.</span></span> <span data-ttu-id="f526d-293">メッセージは、**X** データ モデル フィールドのバインドに **Y** データソースを参照するパスが含まれているが、このデータ ソースは見つからないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-293">The message states that the binding of the **X** data model field contains the path that refers to the **Y** data source, but this data source isn't found.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="f526d-294">自動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-294">Automatic resolution</span></span>

<span data-ttu-id="f526d-295">**バインドの解除** を選択して、欠落したデータ ソース バインドを削除することで、この問題を自動的に修正します。</span><span class="sxs-lookup"><span data-stu-id="f526d-295">Select **Unbind** to automatically fix this issue by removing the missing data source binding.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="f526d-296">手動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-296">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="f526d-297">オプション 1</span><span class="sxs-lookup"><span data-stu-id="f526d-297">Option 1</span></span>

<span data-ttu-id="f526d-298">**X** データ モデル フィールドのバインドを解除して、存在しない **Y** データ ソースを参照しないようにします。</span><span class="sxs-lookup"><span data-stu-id="f526d-298">Unbind the **X** data model field to stop referring to the nonexistent **Y** data source.</span></span>

#### <a name="option-2"></a><span data-ttu-id="f526d-299">オプション 2</span><span class="sxs-lookup"><span data-stu-id="f526d-299">Option 2</span></span>

<span data-ttu-id="f526d-300">ER モデル マッピング デザイナーのデータ ソース ペインで、**Y** データ ソースを再度追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-300">In the data sources pane of the ER model-mapping designer, add the **Y** data source again.</span></span>

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a><span data-ttu-id="f526d-301">FILTER 関数による式の実行可能性</span><span class="sxs-lookup"><span data-stu-id="f526d-301">Executability of an expression with FILTER function</span></span>

<span data-ttu-id="f526d-302">組み込み [FILTER](er-functions-list-filter.md) ER 関数は、アプリケーション テーブル、ビュー、またはデータ エンティティにアクセスするために使用され、1 回の SQL 呼び出しを行うことで、必要なデータをレコードの一覧として取得します。</span><span class="sxs-lookup"><span data-stu-id="f526d-302">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="f526d-303">**レコード リスト** タイプのデータソース は、この関数の引数として使用され、呼び出しのアプリケーション ソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-303">A data source of the **Record list** type is used as an argument of this function and specifies the application source for the call.</span></span> <span data-ttu-id="f526d-304">ERは、`FILTER` 関数で参照されるデータ ソースに対して直接 SQL クエリを確立できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-304">ER checks whether a direct SQL query can be established to a data source that is referred to in the `FILTER` function.</span></span> <span data-ttu-id="f526d-305">直接クエリを確立できない場合、ER モデル マッピング デザイナーで検証エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f526d-305">If a direct query can't be established, a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="f526d-306">受信するメッセージは、`FILTER` 関数を含む ER 式を実行時に実行できないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-306">The message that you receive states that the ER expression that includes the `FILTER` function can't be run at runtime.</span></span> 

<span data-ttu-id="f526d-307">次の手順は、この問題がどのように発生するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-307">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="f526d-308">ER モデル マッピング コンポーネントの構成を開始します。</span><span class="sxs-lookup"><span data-stu-id="f526d-308">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="f526d-309">**Dynamics 365 for Operations \\ テーブル レコード** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-309">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="f526d-310">新しいデータ ソースに **Vendor** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-310">Name the new data source **Vendor**.</span></span> <span data-ttu-id="f526d-311">**テーブル** フィールドで、**VendTable** を選択して、このデータ ソースが VendTable テーブルを要求するように指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-311">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="f526d-312">**計算済フィールド** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-312">Add a data source of the **Calculated field** type.</span></span>
5. <span data-ttu-id="f526d-313">新しいデータ ソースに **FilteredVendor** と名前を付けて、式 `FILTER(Vendor, Vendor.AccountNum="US-101")` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-313">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="f526d-314">**検証** を選択して、**モデル マッピング デザイナー** ページで編集可能なモデル マッピング コンポーネントを検査し、**Vendor** データ ソースの `FILTER(Vendor, Vendor.AccountNum="US-101")` 式を照会できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-314">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>
7. <span data-ttu-id="f526d-315">**計算済フィールド** タイプの入れ子になったフィールドを追加して、**Vendor** データ ソースを変更し、トリムされた仕入先番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="f526d-315">Modify the **Vendor** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="f526d-316">新しい入れ子になったフィールドに **$AccNumber** と名前を付けて、式 `TRIM(Vendor.AccountNum)` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-316">Name the new nested field **$AccNumber**, and configure it so that it contains the expression `TRIM(Vendor.AccountNum)`.</span></span>
9. <span data-ttu-id="f526d-317">**検証** を選択して、**モデル マッピング デザイナー** ページで編集可能なモデル マッピング コンポーネントを検査し、**Vendor** データ ソースの `FILTER(Vendor, Vendor.AccountNum="US-101")` 式を照会できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-317">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>

    ![モデル マッピング デザイナー ページで式を照会できることを確認する](./media/er-components-inspections-04.gif)

10. <span data-ttu-id="f526d-319">**Vendor** データ ソースには、**FilteredVendor** データソースの式を直接 SQL ステートメントに変換できない **計算済フィールド** タイプの入れ子になったフィールドが含まれているため、検証エラーが発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-319">Notice that a validation error occurs, because the **Vendor** data source contains a nested field of the **Calculated field** type that doesn't allow the expression of the **FilteredVendor** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="f526d-320">次の図は、警告を無視し、**実行** を選択して、モデル マッピングを使用するように構成された形式を実行した場合に発生するランタイム エラーを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-320">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model-mapping.</span></span>

![形式デザイナー ページで編集可能な形式を実行したときに発生するランタイム エラー](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a><span data-ttu-id="f526d-322">自動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-322">Automatic resolution</span></span>

<span data-ttu-id="f526d-323">この問題を自動的に修正するオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="f526d-323">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="f526d-324">手動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-324">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="f526d-325">オプション 1</span><span class="sxs-lookup"><span data-stu-id="f526d-325">Option 1</span></span>

<span data-ttu-id="f526d-326">**計算済フィールド** タイプの入れ子になったフィールドを **Vendor** データ ソースに追加するのではなく、**$AccNumber** の入れ子になったフィールドを **FilteredVendor** データ ソースに追加し、式 `TRIM(FilteredVendor.AccountNum)` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-326">Instead of adding a nested field of the **Calculated field** type to the **Vendor** data source, add the **$AccNumber** nested field to the **FilteredVendor** data source, and configure it so that it contains the expression `TRIM(FilteredVendor.AccountNum)`.</span></span> <span data-ttu-id="f526d-327">このようにして、`FILTER(Vendor, Vendor.AccountNum="US-101")` 式を SQL レベルで実行し、**$AccNumber** の入れ子になったフィールドを後で計算することができます。</span><span class="sxs-lookup"><span data-stu-id="f526d-327">In this way, the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="f526d-328">オプション 2</span><span class="sxs-lookup"><span data-stu-id="f526d-328">Option 2</span></span>

<span data-ttu-id="f526d-329">**FilteredVendor** データ ソースの式を `FILTER(Vendor, Vendor.AccountNum="US-101")` から `WHERE(Vendor, Vendor.AccountNum="US-101")` に変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-329">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="f526d-330">すべてのレコードがフェッチされ、必要なレコードの選択がメモリ内で行われるため、大量のデータ (トランザクション テーブル) があるテーブルの式を変更することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="f526d-330">We don't recommend that you change the expression for a table that has a large volume of data (transactional table), because all records will be fetched, and selection of the required records will be done in memory.</span></span> <span data-ttu-id="f526d-331">したがって、この方法ではパフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f526d-331">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="f526d-332">詳細については、[WHERE ER 関数](er-functions-list-where.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-332">For more information, see [WHERE ER function](er-functions-list-where.md).</span></span>

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a><span data-ttu-id="f526d-333">GROUPBY データ ソースの実行可能性</span><span class="sxs-lookup"><span data-stu-id="f526d-333">Executability of a GROUPBY data source</span></span>

<span data-ttu-id="f526d-334">**GROUPBY** データ ソースは、通常は各グループで 1 つ以上の集計を実行する目的で、クエリ結果をレコードのグループに分割します。</span><span class="sxs-lookup"><span data-stu-id="f526d-334">The **GROUPBY** data source divides the query result into groups of records, usually for the purpose of doing one or more aggregations on each group.</span></span> <span data-ttu-id="f526d-335">すべての **GROUPBY** データ ソースは、データベース レベルまたはメモリ内のいずれかで実行されるように構成できます。</span><span class="sxs-lookup"><span data-stu-id="f526d-335">Every **GROUPBY** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="f526d-336">**GROUPBY** データ ソースが、データベース レベルで実行されるように構成されている場合、ER はそのデータ ソースで参照されているデータ ソースに対して直接 SQL クエリを確立できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-336">When a **GROUPBY** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to a data source that is referred to in that data source.</span></span> <span data-ttu-id="f526d-337">直接クエリを確立できない場合、ER モデル マッピング デザイナーで検証エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f526d-337">If a direct query can't be established, a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="f526d-338">受信するメッセージは、構成された **GROUPBY** データ ソースを実行時に実行できないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-338">The message that you receive states that the configured **GROUPBY** data source can't be run at runtime.</span></span>

<span data-ttu-id="f526d-339">次の手順は、この問題がどのように発生するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-339">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="f526d-340">ER モデル マッピング コンポーネントの構成を開始します。</span><span class="sxs-lookup"><span data-stu-id="f526d-340">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="f526d-341">**Dynamics 365 for Operations \\ テーブル レコード** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-341">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="f526d-342">新しいデータ ソースに **Trans** と名前を付けます。**テーブル** フィールドで、**VendTrans** を選択して、このデータ ソースが VendTrans テーブルを要求するように指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-342">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="f526d-343">**Group by** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-343">Add a data source of the **Group by** type.</span></span>
5. <span data-ttu-id="f526d-344">新しいデータ ソースに **GroupedTrans** と名前を付けて、次のように構成します:</span><span class="sxs-lookup"><span data-stu-id="f526d-344">Name the new data source **GroupedTrans**, and configure it in the following way:</span></span>

    - <span data-ttu-id="f526d-345">グループ化するレコードのソースとして **Trans** データ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-345">Select the **Trans** data source as the source of records that should be grouped.</span></span>
    - <span data-ttu-id="f526d-346">**実行場所** フィールドで **クエリ** を選択し、このデータ ソースをデータベース レベルで実行することを指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-346">In the **Execution location** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    !['Group By' パラメーターの編集ページでデータ ソースの構成](./media/er-components-inspections-05a.gif)

6. <span data-ttu-id="f526d-348">**検証** を選択して、**モデル マッピング デザイナー** ページで編集可能なモデル マッピング コンポーネントを検査し、構成済み **GroupedTrans** データ ソースを照会できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-348">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>
7. <span data-ttu-id="f526d-349">**計算済フィールド** タイプの入れ子になったフィールドを追加して、**Trans** データ ソースを変更し、トリムされた仕入先番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="f526d-349">Modify the **Trans** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="f526d-350">新しいデータ ソースに **$AccNumber** と名前を付けて、式 `TRIM(Trans.AccountNum)` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-350">Name the new data source **$AccNumber**, and configure it so that it contains the expression `TRIM(Trans.AccountNum)`.</span></span>

    ![モデル マッピング デザイナー ページでのデータ ソースの構成](./media/er-components-inspections-05a.png)

9. <span data-ttu-id="f526d-352">**検証** を選択して、**モデル マッピング デザイナー** ページで編集可能なモデル マッピング コンポーネントを検査し、構成済み **GroupedTrans** データ ソースを照会できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-352">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>

    ![ER モデル マッピング コンポーネントを検証し、構成済みデータ ソース GroupedTrans をモデル マッピング デザイナ ページで照会できることを確認する](./media/er-components-inspections-05b.png)

10. <span data-ttu-id="f526d-354">**Trans** データ ソースには、**GroupedTrans** データソースの呼び出しを直接 SQL ステートメントに変換できない **計算済フィールド** タイプの入れ子になったフィールドが含まれているため、検証エラーが発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-354">Notice that a validation error occurs, because the **Trans** data source contains a nested field of the **Calculated field** type that doesn't allow the call for the **GroupedTrans** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="f526d-355">次の図は、警告を無視し、**実行** を選択して、モデル マッピングを使用するように構成された形式を実行した場合に発生するランタイム エラーを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-355">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model-mapping.</span></span>

![形式デザイナー ページで警告を無視したときに発生するランタイム エラー](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a><span data-ttu-id="f526d-357">自動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-357">Automatic resolution</span></span>

<span data-ttu-id="f526d-358">この問題を自動的に修正するオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="f526d-358">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="f526d-359">手動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-359">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="f526d-360">オプション 1</span><span class="sxs-lookup"><span data-stu-id="f526d-360">Option 1</span></span>

<span data-ttu-id="f526d-361">**計算済フィールド** タイプの入れ子になったフィールドを **Trans** データ ソースに追加するのではなく、**GroupedTrans** データ ソースの **GroupedTrans.lines** 項目に、**$AccNumber** の入れ子になったフィールドを追加し、式 `TRIM(GroupedTrans.lines.AccountNum)` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-361">Instead of adding a nested field of the **Calculated field** type to the **Trans** data source, add the **$AccNumber** nested field for the **GroupedTrans.lines** item of the **GroupedTrans** data source, and configure it so that it contains the expression `TRIM(GroupedTrans.lines.AccountNum)`.</span></span> <span data-ttu-id="f526d-362">このようにして、**GroupedTrans** データ ソースを SQL レベルで実行し、**$AccNumber** の入れ子になったフィールドを後で計算することができます。</span><span class="sxs-lookup"><span data-stu-id="f526d-362">In this way, the **GroupedTrans** data source can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="f526d-363">オプション 2</span><span class="sxs-lookup"><span data-stu-id="f526d-363">Option 2</span></span>

<span data-ttu-id="f526d-364">**GroupedTrans** データ ソースの **実行場所** フィールドの値を **クエリ** から **メモリ内** に変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-364">Change the value of the **Execution location** field for the **GroupedTrans** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="f526d-365">すべてのレコードがフェッチされ、グループと集計がメモリ内で行われるため、大量のデータ (トランザクション テーブル) があるテーブルの値を変更することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="f526d-365">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and grouping and aggregation will be done in memory.</span></span> <span data-ttu-id="f526d-366">したがって、この方法ではパフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f526d-366">Therefore, this approach can cause poor performance.</span></span>

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a><span data-ttu-id="f526d-367">JOIN データ ソースの実行可能性</span><span class="sxs-lookup"><span data-stu-id="f526d-367">Executability of a JOIN data source</span></span>

<span data-ttu-id="f526d-368">[JOIN](er-join-data-sources.md) データ ソースは、関連するフィールドに基づいて 2 つ以上のデータベース テーブルのレコードを組み合わせたものです。</span><span class="sxs-lookup"><span data-stu-id="f526d-368">The [JOIN](er-join-data-sources.md) data source combines records from two or more database tables, based on related fields.</span></span> <span data-ttu-id="f526d-369">すべての **JOIN** データ ソースは、データベース レベルまたはメモリ内のいずれかで実行されるように構成できます。</span><span class="sxs-lookup"><span data-stu-id="f526d-369">Every **JOIN** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="f526d-370">**JOIN** データ ソースが、データベース レベルで実行されるように構成されている場合、ER はそのデータ ソースで参照されているデータ ソースに対して直接 SQL クエリを確立できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-370">When a **JOIN** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to data sources that are referred to in that data source.</span></span> <span data-ttu-id="f526d-371">1 つ以上の参照データ ソースで直接 SQL クエリを確立できない場合、ER モデル マッピング デザイナーで検証エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f526d-371">If a direct SQL query can't be established with at least one referenced data source, a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="f526d-372">受信するメッセージは、構成された **JOIN** データ ソースを実行時に実行できないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-372">The message that you receive states that the configured **JOIN** data source can't be run at runtime.</span></span>

<span data-ttu-id="f526d-373">次の手順は、この問題がどのように発生するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-373">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="f526d-374">ER モデル マッピング コンポーネントの構成を開始します。</span><span class="sxs-lookup"><span data-stu-id="f526d-374">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="f526d-375">**Dynamics 365 for Operations \\ テーブル レコード** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-375">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="f526d-376">新しいデータ ソースに **Vendor** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-376">Name the new data source **Vendor**.</span></span> <span data-ttu-id="f526d-377">**テーブル** フィールドで、**VendTable** を選択して、このデータ ソースが VendTable テーブルを要求するように指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-377">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="f526d-378">**Dynamics 365 for Operations \\ テーブル レコード** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-378">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
5. <span data-ttu-id="f526d-379">新しいデータ ソースに **Trans** と名前を付けます。**テーブル** フィールドで、**VendTrans** を選択して、このデータ ソースが VendTrans テーブルを要求するように指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-379">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
6. <span data-ttu-id="f526d-380">**計算済フィールド** タイプのデータソースを **Vendor** データソースの入れ子になったフィールドとして追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-380">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
7. <span data-ttu-id="f526d-381">新しいデータ ソースに **FilteredTrans** と名前を付けて、式 `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-381">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
8. <span data-ttu-id="f526d-382">**Join** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-382">Add a data source of the **Join** type.</span></span>
9. <span data-ttu-id="f526d-383">新しいデータ ソースに **JoinedList** と名前を付けて、次のように構成します:</span><span class="sxs-lookup"><span data-stu-id="f526d-383">Name the new data source **JoinedList**, and configure it in the following way:</span></span>

    1. <span data-ttu-id="f526d-384">**Vendor** データ ソースを、結合するレコードの最初のセットとして追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-384">Add the **Vendor** data source as the first set of records to join.</span></span>
    2. <span data-ttu-id="f526d-385">**Vendor.FilteredTrans** データ ソースを、結合するレコードの 2 番目のセットとして追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-385">Add the **Vendor.FilteredTrans** data source as the second set of records to join.</span></span> <span data-ttu-id="f526d-386">タイプとして **INNER** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-386">Select **INNER** as the type.</span></span>
    3. <span data-ttu-id="f526d-387">**実行** フィールドで **クエリ** を選択し、このデータ ソースをデータベース レベルで実行することを指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-387">In the **Execute** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![Join デザイナー ページでのデータ ソースの構成](./media/er-components-inspections-06a.gif)

10. <span data-ttu-id="f526d-389">**検証** を選択して、**モデル マッピング デザイナー** ページで編集可能なモデル マッピング コンポーネントを検査し、構成済み **JoinedList** データ ソースを照会できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-389">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>
11. <span data-ttu-id="f526d-390">**Vendor.FilteredTrans** データ ソースの式を `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` から `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` に変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-390">Change the expression of the **Vendor.FilteredTrans** data source from `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` to `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
12. <span data-ttu-id="f526d-391">**検証** を選択して、**モデル マッピング デザイナー** ページで編集可能なモデル マッピング コンポーネントを検査し、構成済み **JoinedList** データ ソースを照会できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-391">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>

    ![編集可能なモデル マッピング コンポーネントを検証し、モデル マッピング デザイナー ページで JoinedList データ ソースを照会できることを確認します](./media/er-components-inspections-06b.png)

13. <span data-ttu-id="f526d-393">**Vendor.FilteredTrans** データ ソースの式を直接 SQL 呼び出しに変換できないため、検証エラーが発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-393">Notice that a validation error occurs, because the expression of the **Vendor.FilteredTrans** data source can't be translated to the direct SQL call.</span></span> <span data-ttu-id="f526d-394">さらに、直接 SQL 呼び出しでは、**JoinedList** データソースに対する呼び出しを、直接 SQL ステートメントに変換することはできません。</span><span class="sxs-lookup"><span data-stu-id="f526d-394">Additionally, the direct SQL call doesn't allow the call for the **JoinedList** data source to be translated to the direct SQL statement.</span></span>

    ![モデル マッピング デザイナー ページで JoinedList データ ソースの検証に失敗したため発生したランタイム エラー](./media/er-components-inspections-06c.png)

<span data-ttu-id="f526d-396">次の図は、警告を無視し、**実行** を選択して、モデル マッピングを使用するように構成された形式を実行した場合に発生するランタイム エラーを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-396">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model-mapping.</span></span>

![形式デザイナー ページでの編集可能な形式の実行](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="f526d-398">自動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-398">Automatic resolution</span></span>

<span data-ttu-id="f526d-399">この問題を自動的に修正するオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="f526d-399">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="f526d-400">手動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-400">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="f526d-401">オプション 1</span><span class="sxs-lookup"><span data-stu-id="f526d-401">Option 1</span></span>

<span data-ttu-id="f526d-402">警告に従って、**Vendor.FilteredTrans** データ ソースの式を `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` から `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` に戻します。</span><span class="sxs-lookup"><span data-stu-id="f526d-402">Change the expression of the **Vendor.FilteredTrans** data source from `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` back to `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, as the warning advised.</span></span>

![モデル マッピング デザイナー ページでデータ ソースの式を更新](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a><span data-ttu-id="f526d-404">オプション 2</span><span class="sxs-lookup"><span data-stu-id="f526d-404">Option 2</span></span>

<span data-ttu-id="f526d-405">**JoinedList** データ ソースの **実行** フィールドの値を **クエリ** から **メモリ内** に変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-405">Change the value of the **Execute** field for the **JoinedList** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="f526d-406">すべてのレコードがフェッチされ、結合がメモリ内で行われるため、大量のデータ (トランザクション テーブル) があるテーブルの値を変更することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="f526d-406">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and the join occurs in memory.</span></span> <span data-ttu-id="f526d-407">したがって、この方法ではパフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f526d-407">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="f526d-408">このリスクを通知する検証警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f526d-408">A validation warning is shown to inform you about this risk.</span></span>

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a><span data-ttu-id="f526d-409">FILTER 関数 対 WHERE 関数の優先度</span><span class="sxs-lookup"><span data-stu-id="f526d-409">Preferability of FILTER vs WHERE function</span></span>

<span data-ttu-id="f526d-410">組み込み [FILTER](er-functions-list-filter.md) ER 関数は、アプリケーション テーブル、ビュー、またはデータ エンティティにアクセスするために使用され、1 回の SQL 呼び出しを行うことで、必要なデータをレコードの一覧として取得します。</span><span class="sxs-lookup"><span data-stu-id="f526d-410">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="f526d-411">[WHERE](er-functions-list-where.md) 関数は、指定されたソースからすべてのレコードをフェッチし、メモリ内でレコード選択を行います。</span><span class="sxs-lookup"><span data-stu-id="f526d-411">The [WHERE](er-functions-list-where.md) function fetches all records from the given source and does record selection in memory.</span></span> <span data-ttu-id="f526d-412">**レコード リスト** タイプのデータ ソースは、両方の関数の引数として使用され、レコードを取得するためのソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-412">A data source of the **Record list** type is used as an argument of both functions and specifies a source for getting records.</span></span> <span data-ttu-id="f526d-413">ERは、**WHERE** 関数で参照されるデータ ソースに対して直接 SQL 呼び出しを確立できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-413">ER checks whether a direct SQL call can be established to a data source that is referred to in the **WHERE** function.</span></span> <span data-ttu-id="f526d-414">直接呼び出しを確立できる場合、ER モデル マッピング デザイナーで検証警告が発生します。</span><span class="sxs-lookup"><span data-stu-id="f526d-414">If a direct call can be established, a validation warning occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="f526d-415">受信するメッセージは、効率を向上させるために、**WHERE** 関数の代わりに **FILTER** 関数を使用することを推奨しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-415">The message that you receive recommends that you use the **FILTER** function instead of the **WHERE** function to help improve efficiency.</span></span>

<span data-ttu-id="f526d-416">次の手順は、この問題がどのように発生するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-416">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="f526d-417">ER モデル マッピング コンポーネントの構成を開始します。</span><span class="sxs-lookup"><span data-stu-id="f526d-417">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="f526d-418">**Dynamics 365 for Operations \\ テーブル レコード** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-418">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="f526d-419">新しいデータ ソースに **Trans** と名前を付けます。**テーブル** フィールドで、**VendTrans** を選択して、このデータ ソースが VendTrans テーブルを要求するように指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-419">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="f526d-420">**計算済フィールド** タイプのデータソースを **Vendor** データソースの入れ子になったフィールドとして追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-420">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
5. <span data-ttu-id="f526d-421">新しいデータ ソースに **FilteredTrans** と名前を付けて、式 `WHERE(Trans, Trans.AccountNum="US-101")` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-421">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `WHERE(Trans, Trans.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="f526d-422">**Dynamics 365 for Operations \\ テーブル レコード** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-422">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="f526d-423">新しいデータ ソースに **Vendor** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-423">Name the new data source **Vendor**.</span></span> <span data-ttu-id="f526d-424">**テーブル** フィールドで、**VendTable** を選択して、このデータ ソースが VendTable テーブルを要求するように指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-424">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="f526d-425">**計算済フィールド** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-425">Add a data source of the **Calculated field** type.</span></span>
9. <span data-ttu-id="f526d-426">新しいデータ ソースに **FilteredVendor** と名前を付けて、式 `WHERE(Vendor, Vendor.AccountNum="US-101")` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-426">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span>
10. <span data-ttu-id="f526d-427">**検証** を選択して、**モデル マッピング デザイナー** ページで編集可能なモデル マッピング コンポーネントを検査します。</span><span class="sxs-lookup"><span data-stu-id="f526d-427">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![検証して、モデル マッピング デザイナー ページで編集可能なモデル マッピング コンポーネントを検査する](./media/er-components-inspections-07a.png)

11. <span data-ttu-id="f526d-429">検証の警告は、**FilteredVendor** および **FilteredTrans** データソースに対して **WHERE** 関数ではなく **FILTER** 機能を使用することを推奨しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-429">Notice that validation warnings recommend that you use the **FILTER** function instead of the **WHERE** function for the **FilteredVendor** and **FilteredTrans** data sources.</span></span>

    ![モデル マッピング デザイナー ページで、WHERE 関数の代わりに FILTER 関数を推奨する検証警告](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="f526d-431">自動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-431">Automatic resolution</span></span>

<span data-ttu-id="f526d-432">**修正** を選択して、このタイプの検査の **警告** タブにあるグリッドに表示されるすべてのデータ ソースの式で、**WHERE** 関数を **FILTER** 関数に自動的に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="f526d-432">Select **Fix** to automatically replace the **WHERE** function with the **FILTER** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="f526d-433">または、グリッドで 1 つの警告の行を選択し、**選択した修正** を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="f526d-433">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="f526d-434">この場合、式は、選択された警告で説明されているデータ ソースでのみ自動的に変更されます。</span><span class="sxs-lookup"><span data-stu-id="f526d-434">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![[修正] を選択すると、モデル マッピング デザイナー ページで、WHERE 関数が FILTER 関数に自動的に置き換えられます](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a><span data-ttu-id="f526d-436">手動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-436">Manual resolution</span></span>

<span data-ttu-id="f526d-437">**WHERE** 関数を **FILTER** 関数に置き換えることで、検証グリッド内のすべてのデータ ソースの式を手動で調整できます。</span><span class="sxs-lookup"><span data-stu-id="f526d-437">You can manually adjust the expressions of all the data sources in the validation grid by replacing the **WHERE** function with the **FILTER** function.</span></span>

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a><span data-ttu-id="f526d-438">ALLITEMSQUERY 関数 対 ALLITEMS 関数の優先度</span><span class="sxs-lookup"><span data-stu-id="f526d-438">Preferability of ALLITEMSQUERY vs ALLITEMS function</span></span>

<span data-ttu-id="f526d-439">組み込みの [ALLITEMS](er-functions-list-allitems.md) と [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ER 関数は、指定したパスに一致するすべての項目を表すレコードの一覧から成るフラット化された **レコード リスト** の値を返します。</span><span class="sxs-lookup"><span data-stu-id="f526d-439">The built-in [ALLITEMS](er-functions-list-allitems.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ER functions return a flattened **Record list** value that consists of a list of records that represent all items that match the specified path.</span></span> <span data-ttu-id="f526d-440">ER は、**ALLITEMS** 関数で参照されるデータ ソースに対して直接 SQL 呼び出しを確立できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-440">ER checks whether a direct SQL call can be established to a data source that is referred to in the **ALLITEMS** function.</span></span> <span data-ttu-id="f526d-441">直接呼び出しを確立できる場合、ER モデル マッピング デザイナーで検証警告が発生します。</span><span class="sxs-lookup"><span data-stu-id="f526d-441">If a direct call can be established, a validation warning occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="f526d-442">受信するメッセージは、効率を向上させるために、**ALLITEMS** 関数の代わりに **ALLITEMSQUERY** 関数を使用することを推奨しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-442">The message that you receive recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function to help improve efficiency.</span></span>

<span data-ttu-id="f526d-443">次の手順は、この問題がどのように発生するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-443">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="f526d-444">ER モデル マッピング コンポーネントの構成を開始します。</span><span class="sxs-lookup"><span data-stu-id="f526d-444">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="f526d-445">**Dynamics 365 for Operations \\ テーブル レコード** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-445">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="f526d-446">新しいデータ ソースに **Vendor** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-446">Name the new data source **Vendor**.</span></span> <span data-ttu-id="f526d-447">**テーブル** フィールドで、**VendTable** を選択して、このデータ ソースが VendTable テーブルを要求するように指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-447">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="f526d-448">**計算済みフィールド** タイプのデータ ソースを追加して、複数の仕入先のレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="f526d-448">Add a data source of the **Calculated field** type to get records for several vendors.</span></span>
5. <span data-ttu-id="f526d-449">新しいデータ ソースに **FilteredVendor** と名前を付けて、式 `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-449">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.</span></span>
6. <span data-ttu-id="f526d-450">**計算済みフィールド** タイプのデータ ソースを追加して、フィルターされたすべての仕入先のトランザクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="f526d-450">Add a data source of the **Calculated field** type to get transactions of all filtered vendors.</span></span>
7. <span data-ttu-id="f526d-451">新しいデータ ソースに **FilteredVendorTrans** と名前を付けて、式 `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-451">Name the new data source **FilteredVendorTrans**, and configure it so that it contains the expression `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.</span></span>
8. <span data-ttu-id="f526d-452">**検証** を選択して、**モデル マッピング デザイナー** ページで編集可能なモデル マッピング コンポーネントを検査します。</span><span class="sxs-lookup"><span data-stu-id="f526d-452">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![モデル マッピング デザイナー ページ、[検証] ボタン](./media/er-components-inspections-08a.png)

9. <span data-ttu-id="f526d-454">検証警告が発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-454">Notice that a validation warning occurs.</span></span> <span data-ttu-id="f526d-455">このメッセージでは、**FilteredVendorTrans** データ ソースに **ALLITEMS** 関数の代わりに **ALLITEMSQUERY** 関数を使用することを推奨しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-455">The message recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function for the **FilteredVendorTrans** data source.</span></span>

    ![モデル マッピング デザイナー ページの ER モデル マッピング コンポーネントで、ALLITEMS 関数の代わりに ALLITEMSQUERY 関数を使用する場合の検証警告](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="f526d-457">自動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-457">Automatic resolution</span></span>

<span data-ttu-id="f526d-458">**修正** を選択して、このタイプの検査の **警告** タブにあるグリッドに表示されるすべてのデータ ソースの式で、**ALLITEMS** 関数を **ALLITEMSQUERY** 関数に自動的に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="f526d-458">Select **Fix** to automatically replace the **ALLITEMS** function with the **ALLITEMSQUERY** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="f526d-459">または、グリッドで 1 つの警告の行を選択し、**選択した修正** を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="f526d-459">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="f526d-460">この場合、式は、選択された警告で説明されているデータ ソースでのみ自動的に変更されます。</span><span class="sxs-lookup"><span data-stu-id="f526d-460">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![モデル マッピング デザイナー ページで、[選択した修正] を選択する](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a><span data-ttu-id="f526d-462">手動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-462">Manual resolution</span></span>

<span data-ttu-id="f526d-463">**ALLITEMS** 関数を **ALLITEMSQUERY** 関数に置き換えることで、検証グリッドに記載されているすべてのデータ ソースの式を手動で調整できます。</span><span class="sxs-lookup"><span data-stu-id="f526d-463">You can manually adjust the expressions of all the data sources that are mentioned in the validation grid by replacing the **ALLITEMS** function with the **ALLITEMSQUERY** function.</span></span>

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a><span data-ttu-id="f526d-464">空リストの場合の考慮</span><span class="sxs-lookup"><span data-stu-id="f526d-464">Consideration of empty list cases</span></span>

<span data-ttu-id="f526d-465">ER 形式またはモデル マッピング コンポーネントを構成して、**レコード リスト** タイプのデータ ソースのフィールド値を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="f526d-465">You can configure your ER format or model-mapping component to get the field value of a data source of the **Record list** type.</span></span> <span data-ttu-id="f526d-466">ERは、存在しないレコードのフィールドから値がフェッチされるときのランタイム エラーを防ぐために、呼び出されるデータ ソースにレコードが含まれていない (つまり空である) 場合を考慮して設計されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-466">ER checks whether your design considers the case where a data source that is called contains no records (that is, it's empty), to prevent runtime errors when a value is fetched from a field of a nonexistent record.</span></span>

<span data-ttu-id="f526d-467">次の手順は、この問題がどのように発生するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-467">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="f526d-468">ER データ モデル、ER モデル マッピング、 ER 形式コンポーネントの構成を同時に開始します。</span><span class="sxs-lookup"><span data-stu-id="f526d-468">Start to configure the ER data model, the ER model-mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="f526d-469">データ モデル ツリーで、**Root3** という名前のルート項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-469">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="f526d-470">**レコード リスト** タイプの入れ子になった項目を追加して、**Root3** 項目を変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-470">Modify the **Root3** item by adding a nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="f526d-471">新しい入れ子になった項目 **Vendor** に名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-471">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="f526d-472">次の方法で **Vendor** 項目を変更します:</span><span class="sxs-lookup"><span data-stu-id="f526d-472">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="f526d-473">**文字列** タイプの入れ子になったフィールドを追加し、**Name** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-473">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="f526d-474">**文字列** タイプの入れ子になったフィールドを追加し、**AccountNumber** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-474">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![データ モデル ページで入れ子になったフィールドの追加](./media/er-components-inspections-09a.png)

6. <span data-ttu-id="f526d-476">モデル マッピング データ ソース ペインで、**Dynamics 365 for Operations \\ テーブル レコード** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-476">In the model-mapping data sources pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="f526d-477">新しいデータ ソースに **Vendor** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-477">Name the new data source **Vendor**.</span></span> <span data-ttu-id="f526d-478">**テーブル** フィールドで、**VendTable** を選択して、このデータ ソースが VendTable テーブルを要求するように指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-478">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="f526d-479">**全般 \\ ユーザー入力パラメーター** タイプのデータ ソースを追加し、ランタイム ダイアログ ボックスで仕入先アカウントを検索します。</span><span class="sxs-lookup"><span data-stu-id="f526d-479">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
9. <span data-ttu-id="f526d-480">新しいデータ ソースに **RequestedAccountNum** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-480">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="f526d-481">**ラベル** フィールドに、**仕入先番号** を入力します。</span><span class="sxs-lookup"><span data-stu-id="f526d-481">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="f526d-482">**操作のデータ型名** フィールドは、既定値の **説明** のままにします。</span><span class="sxs-lookup"><span data-stu-id="f526d-482">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="f526d-483">**計算済フィールド** タイプのデータ ソースを追加して、照会する仕入先をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="f526d-483">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="f526d-484">新しいデータ ソースに **FilteredVendor** と名前を付けて、式 `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-484">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="f526d-485">次の方法で、構成されたデータ ソースにデータ モデル項目をバインドします:</span><span class="sxs-lookup"><span data-stu-id="f526d-485">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="f526d-486">**FilteredVendor** を **Vendor** にバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-486">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="f526d-487">**FilteredVendor.AccountNum** を **Vendor.AccountNumber** にバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-487">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>
    - <span data-ttu-id="f526d-488">**FilteredVendor.'name()'** を **Vendor.Name** にバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-488">Bind **FilteredVendor.'name()'** to **Vendor.Name**.</span></span>

    ![モデル マッピング デザイナー ページでのデータ モデル項目のバインド](./media/er-components-inspections-09b.png)

13. <span data-ttu-id="f526d-490">形式構造ツリーで、次の項目を追加して、仕入先の詳細を含む送信ドキュメントを XML 形式で生成します:</span><span class="sxs-lookup"><span data-stu-id="f526d-490">In the format structure tree, add the following items to generate an outbound document in XML format that contains the vendor details:</span></span>

    1. <span data-ttu-id="f526d-491">**Statement** ルート XML 要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-491">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="f526d-492">**Statement** XML 要素の場合は、入れ子になった **Party** XML 要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-492">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="f526d-493">**Party** XML 要素の場合は、次の入れ子になった XML 属性を追加します:</span><span class="sxs-lookup"><span data-stu-id="f526d-493">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="f526d-494">氏名</span><span class="sxs-lookup"><span data-stu-id="f526d-494">Name</span></span>
        - <span data-ttu-id="f526d-495">AccountNum</span><span class="sxs-lookup"><span data-stu-id="f526d-495">AccountNum</span></span>

14. <span data-ttu-id="f526d-496">次の方法で、形式要素を指定されたデータ ソースにバインドします:</span><span class="sxs-lookup"><span data-stu-id="f526d-496">Bind format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="f526d-497">**Statement\\Party\\Name** 形式要素を **model.Vendor.Name** データ ソース フィールドにバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-497">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="f526d-498">**Statement\\Party\\AccountNum** 形式要素を **model.Vendor.AccountNumber** データ ソース フィールドにバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-498">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="f526d-499">**検証** を選択して、**形式デザイナー** ページで編集可能な形式コンポーネントを検査します。</span><span class="sxs-lookup"><span data-stu-id="f526d-499">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![形式デザイナー ページでデータ ソースにバインドした形式要素の検証](./media/er-components-inspections-09c.png)

16. <span data-ttu-id="f526d-501">検証エラーが発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-501">Notice that a validation error occurs.</span></span> <span data-ttu-id="f526d-502">メッセージは、`model.Vendor` リストが空の場合、実行時に、構成済みの **Statement\\Party\\Name** と **Statement\\Party\\AccountNum** に対してエラーがスローされる可能性があることを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-502">The message states that an error might be thrown for the configured **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format components at runtime if the `model.Vendor` list is empty.</span></span>

    ![構成済みの形式コンポーネントの潜在的なエラーを通知する検証エラー](./media/er-components-inspections-09d.png)

<span data-ttu-id="f526d-504">次の図は、警告を無視し、**実行** を選択して形式を実行し、存在しない仕入先のアカウント番号を選択した場合に発生するランタイム エラーを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-504">The following illustration shows the runtime error that occurs if you ignore the warning, select **Run** to run the format, and select the account number of a nonexistent vendor.</span></span> <span data-ttu-id="f526d-505">要求された仕入先が存在しないため、`model.Vendor` リストは空になります (つまり、レコードが含まれていません)。</span><span class="sxs-lookup"><span data-stu-id="f526d-505">Because the requested vendor doesn't exist, the `model.Vendor` list will be empty (that is, it will contain no records).</span></span>

![形式マッピングの実行中に発生したランタイム エラー](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="f526d-507">自動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-507">Automatic resolution</span></span>

<span data-ttu-id="f526d-508">**警告** タブのグリッドで選択した行に対して、**バインドの解除** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="f526d-508">For the selected row in the grid on the **Warnings** tab, you can select **Unbind**.</span></span> <span data-ttu-id="f526d-509">**パス** 列でポイントされているバインドは、形式要素から自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="f526d-509">The binding that is pointed to in the **Path** column is automatically removed from the format elements.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="f526d-510">手動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-510">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="f526d-511">オプション 1</span><span class="sxs-lookup"><span data-stu-id="f526d-511">Option 1</span></span>

<span data-ttu-id="f526d-512">**Statement\\Party\\Name** 形式要素を `model.Vendor` データ ソース項目にバインドできます。</span><span class="sxs-lookup"><span data-stu-id="f526d-512">You can bind the **Statement\\Party\\Name** format element to the `model.Vendor` data source item.</span></span> <span data-ttu-id="f526d-513">実行時に、このバインドは `model.Vendor` データ ソースを最初に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f526d-513">At runtime, this binding calls the `model.Vendor` data source first.</span></span> <span data-ttu-id="f526d-514">`model.Vendor` が、空のレコード リストを返す場合、入れ子になった形式要素は実行されません。</span><span class="sxs-lookup"><span data-stu-id="f526d-514">When `model.Vendor` returns an empty record list, the nested format elements aren't run.</span></span> <span data-ttu-id="f526d-515">したがって、この形式構成に対して検証警告は発生しません。</span><span class="sxs-lookup"><span data-stu-id="f526d-515">Therefore, no validation warnings occur for this format configuration.</span></span>

![形式デザイナー ページで形式要素をデータ ソース項目にバインドする](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a><span data-ttu-id="f526d-517">オプション 2</span><span class="sxs-lookup"><span data-stu-id="f526d-517">Option 2</span></span>

<span data-ttu-id="f526d-518">**Statement\\Party\\Name** 形式要素のバインドを `model.Vendor.Name` から `FIRSTORNULL(model.Vendor).Name` に変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-518">Change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `FIRSTORNULL(model.Vendor).Name`.</span></span> <span data-ttu-id="f526d-519">更新されたバインドは、**レコード リスト** タイプの `model.Vendor` データ ソースの最初のレコードを、**レコード** タイプの新しいデータ ソースに条件付きで変換します。</span><span class="sxs-lookup"><span data-stu-id="f526d-519">The updated binding conditionally converts the first record of the `model.Vendor` data source of the **Record list** type to a new data source of the **Record** type.</span></span> <span data-ttu-id="f526d-520">この新しいデータ ソースには、同じセットのフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f526d-520">This new data source contains the same set of fields.</span></span>

- <span data-ttu-id="f526d-521">`model.Vendor` データ ソースに使用可能なレコードが少なくとも 1 つある場合、そのレコードのフィールドには、`model.Vendor` データ ソースの最初のレコードのフィールドの値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="f526d-521">If at least one record is available in the `model.Vendor` data source, the fields of that record are filled with the values of the fields of the first record of the `model.Vendor` data source.</span></span> <span data-ttu-id="f526d-522">この場合、更新されたバインドは仕入先名を返します。</span><span class="sxs-lookup"><span data-stu-id="f526d-522">In this case, the updated binding returns the vendor name.</span></span>
- <span data-ttu-id="f526d-523">それ以外の場合は、作成されたレコードのすべてのフィールドは、そのフィールドのデータ型の既定値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="f526d-523">Otherwise, every field of the record that is created is filled with the default value for the data type of that field.</span></span> <span data-ttu-id="f526d-524">この場合は、**文字列** データ型の既定値として空白文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f526d-524">In this case, the blank string is returned as the default value of the **String** data type.</span></span>

<span data-ttu-id="f526d-525">したがって、**Statement\\Party\\Name** の形式要素が、`FIRSTORNULL(model.Vendor).Name` 式にバインドされても、検証の警告は発生しません。</span><span class="sxs-lookup"><span data-stu-id="f526d-525">Therefore, no validation warnings occur for the **Statement\\Party\\Name** format element when it's bound to the `FIRSTORNULL(model.Vendor).Name` expression.</span></span>

![変更されたバインドにより、形式デザイナー ページで検証の警告を解決する](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a><span data-ttu-id="f526d-527">オプション 3</span><span class="sxs-lookup"><span data-stu-id="f526d-527">Option 3</span></span>

<span data-ttu-id="f526d-528">**レコード リスト** タイプの `model.Vendor` データ ソースが、レコードを返さないときに (テキスト この例では **使用できません**)、生成されるドキュメントに入力されるデータを明示的に指定する場合は、**Statement\\Party\\Name** 形式要素のバインドを `model.Vendor.Name` から `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")` に変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-528">If you want to explicitly specify the data that is entered in a generated document when the `model.Vendor` data source of the **Record list** type returns no records (the text **Not available** in this example), change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`.</span></span> <span data-ttu-id="f526d-529">式 `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")` を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="f526d-529">You can also use the expression `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.</span></span>

### <a name="additional-consideration"></a><a id="i9a"></a><span data-ttu-id="f526d-530">その他の考慮事項</span><span class="sxs-lookup"><span data-stu-id="f526d-530">Additional consideration</span></span>

<span data-ttu-id="f526d-531">検査では、別の潜在的な問題についても警告します。</span><span class="sxs-lookup"><span data-stu-id="f526d-531">The inspection also warns you about another potential issue.</span></span> <span data-ttu-id="f526d-532">既定では、**Statement\\Party\\Name** と **Statement\\Party\\AccountNum** の形式要素を **レコード リスト** タイプの `model.Vendor` データ ソースの適切なフィールドにバインドすると、これらのバインドが実行され、`model.Vendor` データ ソースの最初のレコードの適切なフィールドの値を取得します (リストが空でない場合)。</span><span class="sxs-lookup"><span data-stu-id="f526d-532">By default, as you bind the **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format elements to the appropriate fields of the `model.Vendor` data source of the **Record list** type, those bindings will be run and will take the values of the appropriate fields of the first record of the `model.Vendor` data source, if that list isn't empty.</span></span>

<span data-ttu-id="f526d-533">**Statement\\Party** 形式要素を `model.Vendor` データ ソースにバインドしていないため、形式の実行中に **Statement\\Party** 要素は、`model.Vendor` データ ソースの各レコードに対して反復処理されません。</span><span class="sxs-lookup"><span data-stu-id="f526d-533">Because you haven't bound the **Statement\\Party** format element with the `model.Vendor` data source, the **Statement\\Party** element won't be iterated for every record of the `model.Vendor` data source during format execution.</span></span> <span data-ttu-id="f526d-534">代わりに、このリストに複数のレコードが含まれている場合、生成されるドキュメントには、レコード リストの最初のレコードからのみ情報が入力されます。</span><span class="sxs-lookup"><span data-stu-id="f526d-534">Instead, a generated document will be filled with information from only the first record of the record list, if that list contains multiple records.</span></span> <span data-ttu-id="f526d-535">したがって、形式が `model.Vendor` データ ソースのすべての仕入先に関する情報で、生成されたドキュメントを埋めることが目的の場合に、問題が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="f526d-535">Therefore, there might be an issue if the format is intended to fill a generated document with information about all vendors from the `model.Vendor` data source.</span></span> <span data-ttu-id="f526d-536">この問題を修正するには、**Statement\\Party** 要素を `model.Vendor` データ ソースにバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-536">To fix this issue, bind the **Statement\\Party** element with the `model.Vendor` data source.</span></span>

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a><span data-ttu-id="f526d-537">FILTER 関数による式の実行可能性 (キャッシュ)</span><span class="sxs-lookup"><span data-stu-id="f526d-537">Executability of an expression with FILTER function (caching)</span></span>

<span data-ttu-id="f526d-538">[FILTER](er-functions-list-filter.md) や [ALLITEMSQUERY](er-functions-list-allitemsquery.md) などの、複数の組み込み ER 関数は、アプリケーション テーブル、ビュー、またはデータ エンティティにアクセスするために使用され、1 回の SQL 呼び出しを行うことで、必要なデータをレコードの一覧として取得します。</span><span class="sxs-lookup"><span data-stu-id="f526d-538">Several built-in ER functions, including [FILTER](er-functions-list-filter.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md), are used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="f526d-539">**レコード リスト** タイプのデータソース は、これらの各関数の引数として使用され、呼び出しのアプリケーション ソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-539">A data source of the **Record list** type is used as an argument of each of these functions and specifies an application source for the call.</span></span> <span data-ttu-id="f526d-540">ERは、これらの関数の 1 つで参照されるデータ ソースに対して直接 SQL 呼び出しを確立できるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f526d-540">ER checks whether a direct SQL call can be established to a data source that is referred to in one of these functions.</span></span> <span data-ttu-id="f526d-541">データ ソースが [キャッシュ](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace) としてマークされているために直接呼び出しを確立できない場合、ER モデル マッピング デザイナーで検証エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f526d-541">If a direct call can't be established because the data source was marked as [cached](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="f526d-542">受信するメッセージは、これたの関数の 1 つを含む ER 式を実行時に実行できないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-542">The message that you receive states that the ER expression that contains one of these functions can't be run at runtime.</span></span>

<span data-ttu-id="f526d-543">次の手順は、この問題がどのように発生するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-543">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="f526d-544">ER モデル マッピング コンポーネントの構成を開始します。</span><span class="sxs-lookup"><span data-stu-id="f526d-544">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="f526d-545">**Dynamics 365 for Operations \\ テーブル レコード** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-545">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="f526d-546">新しいデータ ソースに **Vendor** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-546">Name the new data source **Vendor**.</span></span> <span data-ttu-id="f526d-547">**テーブル** フィールドで、**VendTable** を選択して、このデータ ソースが VendTable テーブルを要求するように指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-547">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="f526d-548">**全般 \\ ユーザー入力パラメーター** タイプのデータ ソースを追加し、ランタイム ダイアログ ボックスで仕入先アカウントを検索します。</span><span class="sxs-lookup"><span data-stu-id="f526d-548">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
5. <span data-ttu-id="f526d-549">新しいデータ ソースに **RequestedAccountNum** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-549">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="f526d-550">**ラベル** フィールドに、**仕入先番号** を入力します。</span><span class="sxs-lookup"><span data-stu-id="f526d-550">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="f526d-551">**操作のデータ型名** フィールドは、既定値の **説明** のままにします。</span><span class="sxs-lookup"><span data-stu-id="f526d-551">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
6. <span data-ttu-id="f526d-552">**計算済フィールド** タイプのデータ ソースを追加して、照会する仕入先をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="f526d-552">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
7. <span data-ttu-id="f526d-553">新しいデータ ソースに **FilteredVendor** と名前を付けて、式 `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-553">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
8. <span data-ttu-id="f526d-554">構成済み **Vendor** データ ソースをキャッシュとしてマークします。</span><span class="sxs-lookup"><span data-stu-id="f526d-554">Mark the configured **Vendor** data source as cached.</span></span>

    ![モデル マッピング デザイナー ページでモデル マッピング コンポーネントを構成する](./media/er-components-inspections-10a.gif)

9. <span data-ttu-id="f526d-556">**検証** を選択して、**モデル マッピング デザイナー** ページで編集可能なモデル マッピング コンポーネントを検査します。</span><span class="sxs-lookup"><span data-stu-id="f526d-556">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![モデル マッピング デザイナー ページで、キャッシュ ベンダーのデータ ソースに適用されたフィルター機能を検証する](./media/er-components-inspections-10a.png)

10. <span data-ttu-id="f526d-558">検証エラーが発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-558">Notice that a validation error occurs.</span></span> <span data-ttu-id="f526d-559">このメッセージは、**FILTER** 関数が、キャッシュされた **Vendor** データ ソースに適用できないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-559">The message states that the **FILTER** function can't be applied to the cached **Vendor** data source.</span></span>

<span data-ttu-id="f526d-560">次の図は、警告を無視し **実行** を選択して、形式を実行した場合に、発生するランタイム エラーを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-560">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![形式デザイナー ページで形式マッピングの実行中に発生したランタイム エラー](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="f526d-562">自動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-562">Automatic resolution</span></span>

<span data-ttu-id="f526d-563">この問題を自動的に修正するオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="f526d-563">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="f526d-564">手動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-564">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="f526d-565">オプション 1</span><span class="sxs-lookup"><span data-stu-id="f526d-565">Option 1</span></span>

<span data-ttu-id="f526d-566">**Vendor** データ ソースから **キャッシュ** フラグを削除します。</span><span class="sxs-lookup"><span data-stu-id="f526d-566">Remove the **Cache** flag from the **Vendor** data source.</span></span> <span data-ttu-id="f526d-567">その後、**FilteredVendor** データ ソースは実行可能になりますが、VendTable テーブルで参照される **Vendor** データ ソースは、**FilteredVendor** データ ソースが呼び出されるたびにアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="f526d-567">The **FilteredVendor** data source will then become executable, but the **Vendor** data source that is referred to in the VendTable table will be accessed every time that the **FilteredVendor** data source is called.</span></span>

#### <a name="option-2"></a><span data-ttu-id="f526d-568">オプション 2</span><span class="sxs-lookup"><span data-stu-id="f526d-568">Option 2</span></span>

<span data-ttu-id="f526d-569">**FilteredVendor** データ ソースの式を `FILTER(Vendor, Vendor.AccountNum="US-101")` から `WHERE(Vendor, Vendor.AccountNum="US-101")` に変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-569">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="f526d-570">この場合、VendTable テーブルで参照される **Vendor** データ ソースは、**Vendor** データ ソースの最初の呼び出し中にのみアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="f526d-570">In this case, the **Vendor** data source that is referred to in the VendTable table will be accessed only during the first call of the **Vendor** data source.</span></span> <span data-ttu-id="f526d-571">ただし、レコードの選択はメモリ内で行われます。</span><span class="sxs-lookup"><span data-stu-id="f526d-571">However, the selection of records will be done in memory.</span></span> <span data-ttu-id="f526d-572">したがって、この方法ではパフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f526d-572">Therefore, this approach can cause poor performance.</span></span>

## <a name="missing-binding"></a><a id="i11"></a><span data-ttu-id="f526d-573">バインドの欠落</span><span class="sxs-lookup"><span data-stu-id="f526d-573">Missing binding</span></span>

<span data-ttu-id="f526d-574">ER 形式コンポーネントを構成する場合、基本 ER データ モデルは ER 形式の既定のデータ ソースとして提供されます。</span><span class="sxs-lookup"><span data-stu-id="f526d-574">When you configure an ER format component, the base ER data model is offered as a default data source for the ER format.</span></span> <span data-ttu-id="f526d-575">構成済み ER 形式を実行すると、基本モデルの [既定のモデル マッピング](er-country-dependent-model-mapping.md) が使用され、データ モデルにアプリケーション データが入力されます。</span><span class="sxs-lookup"><span data-stu-id="f526d-575">When the configured ER format is run, the [default model mapping](er-country-dependent-model-mapping.md) for the base model is used to fill the data model with application data.</span></span> <span data-ttu-id="f526d-576">ER 形式デザイナーは、編集可能な形式の既定のモデル マッピングとして、現在選択されているモデル マッピングのどのデータ ソースにもバインドされていないデータ モデル項目に、形式要素をバインドした場合、警告を表示します。</span><span class="sxs-lookup"><span data-stu-id="f526d-576">The ER format designer shows a warning if you bind a format element to a data model item that isn't bound to any data source in the model-mapping that is currently selected as the default model-mapping for the editable format.</span></span> <span data-ttu-id="f526d-577">このタイプのバインドは、実行される形式がバインド要素をアプリケーション データで埋めることができないため、実行時には実行できません。</span><span class="sxs-lookup"><span data-stu-id="f526d-577">This type of binding can't be run at runtime, because the format that runs can't fill a bound element with application data.</span></span> <span data-ttu-id="f526d-578">したがって、実行時にエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f526d-578">Therefore, an error occurs at runtime.</span></span>

<span data-ttu-id="f526d-579">次の手順は、この問題がどのように発生するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-579">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="f526d-580">ER データ モデル、ER モデル マッピング、 ER 形式コンポーネントの構成を同時に開始します。</span><span class="sxs-lookup"><span data-stu-id="f526d-580">Start to configure the ER data model, the ER model-mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="f526d-581">データ モデル ツリーで、**Root3** という名前のルート項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-581">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="f526d-582">**レコード リスト** タイプの新しい入れ子になった項目を追加して、**Root3** 項目を変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-582">Modify the **Root3** item by adding a new nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="f526d-583">新しい入れ子になった項目 **Vendor** に名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-583">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="f526d-584">次の方法で **Vendor** 項目を変更します:</span><span class="sxs-lookup"><span data-stu-id="f526d-584">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="f526d-585">**文字列** タイプの入れ子になったフィールドを追加し、**Name** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-585">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="f526d-586">**文字列** タイプの入れ子になったフィールドを追加し、**AccountNumber** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-586">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![データ モデル ページの仕入先項目に入れ子になったフィールドを追加します](./media/er-components-inspections-11a.png)

6. <span data-ttu-id="f526d-588">モデル マッピング データ ソース ペインで、**Dynamics 365 for Operations \\ テーブル レコード** タイプのデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-588">In the model-mapping data sources pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="f526d-589">新しいデータ ソースに **Vendor** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-589">Name the new data source **Vendor**.</span></span> <span data-ttu-id="f526d-590">**テーブル** フィールドで、**VendTable** を選択して、このデータ ソースが VendTable テーブルを要求するように指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-590">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="f526d-591">**全般 \\ ユーザー入力パラメーター** タイプのデータ ソースを追加し、ランタイム ダイアログ ボックスで仕入先アカウントについて照会します。</span><span class="sxs-lookup"><span data-stu-id="f526d-591">Add a data source of the **General \\ User input parameter** type to inquire about a vendor account in the runtime dialog box.</span></span>
<span data-ttu-id="f526d-592">9 新しいデータ ソースに **RequestedAccountNum** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f526d-592">9 Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="f526d-593">**ラベル** フィールドに、**仕入先番号** を入力します。</span><span class="sxs-lookup"><span data-stu-id="f526d-593">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="f526d-594">**操作のデータ型名** フィールドは、既定値の **説明** のままにします。</span><span class="sxs-lookup"><span data-stu-id="f526d-594">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="f526d-595">**計算済フィールド** タイプのデータ ソースを追加して、照会する仕入先をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="f526d-595">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="f526d-596">新しいデータ ソースに **FilteredVendor** と名前を付けて、式 `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)` を含むように構成します。</span><span class="sxs-lookup"><span data-stu-id="f526d-596">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="f526d-597">次の方法で、構成されたデータ ソースにデータ モデル項目をバインドします:</span><span class="sxs-lookup"><span data-stu-id="f526d-597">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="f526d-598">**FilteredVendor** を **Vendor** にバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-598">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="f526d-599">**FilteredVendor.AccountNum** を **Vendor.AccountNumber** にバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-599">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f526d-600">**Vendor.Name** データ モデル フィールドはバインド解除されたままです。</span><span class="sxs-lookup"><span data-stu-id="f526d-600">The **Vendor.Name** data model field remains unbound.</span></span>

    ![構成されたデータ ソースにバインドされたデータ モデル項目と、モデル マッピング デザイナー ページのデータ モード項目](./media/er-components-inspections-11b.png)

13. <span data-ttu-id="f526d-602">形式構造ツリーで、次の項目を追加して、照会される仕入先の詳細を含む送信ドキュメントを XML 形式で生成します:</span><span class="sxs-lookup"><span data-stu-id="f526d-602">In the format structure tree, add the following items to generate an outbound document in XML format that contains the details of the vendors that are inquired about:</span></span>

    1. <span data-ttu-id="f526d-603">**Statement** ルート XML 要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-603">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="f526d-604">**Statement** XML 要素の場合は、入れ子になった **Party** XML 要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-604">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="f526d-605">**Party** XML 要素の場合は、次の入れ子になった XML 属性を追加します:</span><span class="sxs-lookup"><span data-stu-id="f526d-605">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="f526d-606">氏名</span><span class="sxs-lookup"><span data-stu-id="f526d-606">Name</span></span>
        - <span data-ttu-id="f526d-607">AccountNum</span><span class="sxs-lookup"><span data-stu-id="f526d-607">AccountNum</span></span>

14. <span data-ttu-id="f526d-608">次の方法で、形式要素を指定されたデータ ソースにバインドします:</span><span class="sxs-lookup"><span data-stu-id="f526d-608">Bind the format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="f526d-609">**Statement\\Party** 形式要素を `model.Vendor` データ ソース項目にバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-609">Bind the **Statement\\Party** format element to the `model.Vendor` data source item.</span></span>
    - <span data-ttu-id="f526d-610">**Statement\\Party\\Name** 形式要素を **model.Vendor.Name** データ ソース フィールドにバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-610">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="f526d-611">**Statement\\Party\\AccountNum** 形式要素を **model.Vendor.AccountNumber** データ ソース フィールドにバインドします。</span><span class="sxs-lookup"><span data-stu-id="f526d-611">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="f526d-612">**検証** を選択して、**形式デザイナー** ページで編集可能な形式コンポーネントを検査します。</span><span class="sxs-lookup"><span data-stu-id="f526d-612">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![形式デザイナー ページで ER 形式コンポーネントを検証する](./media/er-components-inspections-11c.png)

16. <span data-ttu-id="f526d-614">検証警告が発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-614">Notice that a validation warning occurs.</span></span> <span data-ttu-id="f526d-615">メッセージは、**model.Vendor.Name** データ ソース フィールドが、形式で使用するように構成されているモデル マッピングのデータ ソースにバインドされていないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-615">The message states that the **model.Vendor.Name** data source field isn't bound to any data source in the model-mapping that is configured to be used by the format.</span></span> <span data-ttu-id="f526d-616">したがって、**Statement\\Party\\Name** 形式要素が実行時に入力されず、ランタイム例外が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f526d-616">Therefore, the **Statement\\Party\\Name** format element might not be filled at runtime, and a runtime exception might occur.</span></span>

    ![形式デザイナー ページで ER 形式コンポーネントを検証する](./media/er-components-inspections-11d.png)

<span data-ttu-id="f526d-618">次の図は、警告を無視し **実行** を選択して、形式を実行した場合に、発生するランタイム エラーを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-618">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![形式デザイナー ページで編集可能な形式を実行する](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="f526d-620">自動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-620">Automatic resolution</span></span>

<span data-ttu-id="f526d-621">この問題を自動的に修正するオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="f526d-621">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="f526d-622">手動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-622">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="f526d-623">オプション 1</span><span class="sxs-lookup"><span data-stu-id="f526d-623">Option 1</span></span>

<span data-ttu-id="f526d-624">**model.Vendor.Name** データ ソース フィールドにバインドを追加して、構成済みモデル マッピングを変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-624">Modify the configured model-mapping by adding a binding for the **model.Vendor.Name** data source field.</span></span>

#### <a name="option-2"></a><span data-ttu-id="f526d-625">オプション 2</span><span class="sxs-lookup"><span data-stu-id="f526d-625">Option 2</span></span>

<span data-ttu-id="f526d-626">**Statement\\Party\\Name** 形式要素のバインドを削除することで、構成済みの形式を変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-626">Modify the configured format by removing a binding for the **Statement\\Party\\Name** format element.</span></span>

## <a name="not-linked-template"></a><a id="i12"></a><span data-ttu-id="f526d-627">リンクされていないテンプレート</span><span class="sxs-lookup"><span data-stu-id="f526d-627">Not linked template</span></span>

<span data-ttu-id="f526d-628">テンプレートを使用して送信ドキュメントを生成するように ER 形式コンポーネントを [手動で](er-fillable-excel.md#manual-entry) 構成する場合は、**Excel\\File** 要素を手動で追加し、必要なテンプレートを編集可能なコンポーネントの添付ファイルとして追加して、追加された **Excel\\File** 要素で、その添付ファイルを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f526d-628">When you [manually](er-fillable-excel.md#manual-entry) configure an ER format component to use a template to generate an outbound document, you must manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="f526d-629">このようにして、実行時に追加された要素で選択したテンプレートを埋めるように指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-629">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="f526d-630">**ドラフト** [状態](general-electronic-reporting.md#component-versioning) で形式コンポーネントのバージョンを構成する場合は、編集可能なコンポーネントにテンプレートをいくつか追加し、**Excel\\File** 要素で各テンプレートを選択して、ER 形式を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="f526d-630">When you configure a format component version in **Draft** [status](general-electronic-reporting.md#component-versioning), you might add several templates to the editable component, and then select each template in the **Excel\\File** element to run the ER format.</span></span> <span data-ttu-id="f526d-631">このようにして、実行時にさまざまなテンプレートがどのように入力されるかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="f526d-631">In this way, you can see how different templates are filled at runtime.</span></span> <span data-ttu-id="f526d-632">**Excel\\File** 要素で選択されていないテンプレートがある場合、ER 形式デザイナーは、編集可能な ER 形式コンポーネント バージョンの状態が **ドラフト** から **完了** に変更されるたときに、これらのテンプレートがそのバージョンから削除されることを警告します。</span><span class="sxs-lookup"><span data-stu-id="f526d-632">If you have templates that aren't selected in any **Excel\\File** elements, the ER format designer warns you that those templates will be deleted from the editable ER format component version when its status is changed from **Draft** to **Completed**.</span></span>

<span data-ttu-id="f526d-633">次の手順は、この問題がどのように発生するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-633">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="f526d-634">ER 形式コンポーネントの構成を開始します。</span><span class="sxs-lookup"><span data-stu-id="f526d-634">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="f526d-635">形式構造ツリーで、**Excel\\File** 要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-635">In the format structure tree, add the **Excel\\File** element.</span></span>
3. <span data-ttu-id="f526d-636">追加した **Excel\\File** 要素の場合、Excel ブック ファイル **A.xlsx** を添付ファイルとして追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-636">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="f526d-637">[ER パラメーター](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) で構成されているドキュメント タイプを使用して、ER 形式テンプレートのストレージを指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-637">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>
4. <span data-ttu-id="f526d-638">**Excel\\File** 要素の場合、別の Excel ブック ファイル **B.xlsx** を添付ファイルとして追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-638">For the **Excel\\File** element, add another Excel workbook file, **B.xlsx**, as an attachment.</span></span> <span data-ttu-id="f526d-639">ブック ファイル A に使用されているのと同じドキュメント タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="f526d-639">Use the same document type that is used for workbook file A.</span></span>
5. <span data-ttu-id="f526d-640">**Excel\\File** 要素で 、ブック ファイル A を選択します。</span><span class="sxs-lookup"><span data-stu-id="f526d-640">In the **Excel\\File** element, select workbook file A.</span></span>
6. <span data-ttu-id="f526d-641">**検証** を選択して、**形式デザイナー** ページで編集可能な形式コンポーネントを検査します。</span><span class="sxs-lookup"><span data-stu-id="f526d-641">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![形式デザイナー ページでブック ファイルの編集可能な形式コンポーネントを検証する](./media/er-components-inspections-12a.gif)

7. <span data-ttu-id="f526d-643">検証警告が発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-643">Notice that a validation warning occurs.</span></span> <span data-ttu-id="f526d-644">メッセージは、ブック ファイル **B.xlsx** がどのコンポーネントにもリンクされておらず、構成バージョンの状態が変更された後に削除されることを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-644">The message states that workbook file **B.xlsx** isn't linked to any components, and that it will be removed after the status of the configuration version is changed.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="f526d-645">自動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-645">Automatic resolution</span></span>

<span data-ttu-id="f526d-646">この問題を自動的に修正するオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="f526d-646">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="f526d-647">手動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-647">Manual resolution</span></span>

<span data-ttu-id="f526d-648">**Excel\\File** 要素にリンクされていないテンプレートをすべて削除して、構成済みの形式を変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-648">Modify the configured format by removing all templates that aren't linked to any **Excel\\File** element.</span></span>

## <a name="not-synced-format"></a><a id="i13"></a><span data-ttu-id="f526d-649">未同期形式</span><span class="sxs-lookup"><span data-stu-id="f526d-649">Not synced format</span></span>

<span data-ttu-id="f526d-650">Excel テンプレートを使用して送信ドキュメントを生成するように、ER 形式コンポーネントを [構成](er-fillable-excel.md) する場合は、**Excel\\File** 要素を手動で追加し、必要なテンプレートを編集可能なコンポーネントの添付ファイルとして追加して、追加された **Excel\\File** 要素で、その添付ファイルを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f526d-650">When you [configure](er-fillable-excel.md) an ER format component to use an Excel template to generate an outbound document, you can manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="f526d-651">このようにして、実行時に追加された要素で選択したテンプレートを埋めるように指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-651">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="f526d-652">追加した Excel テンプレートは外部で設計されているので、編集可能な ER 形式には、追加したテンプレートにない Excel 名が含まれる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f526d-652">Because the added Excel template has been externally designed, the editable ER format might contain Excel names that are missing from the added template.</span></span> <span data-ttu-id="f526d-653">ER 形式デザイナーは、追加した Excel テンプレートに含まれていない名前を参照する ER 形式要素のプロパティ間の不整合について警告します。</span><span class="sxs-lookup"><span data-stu-id="f526d-653">The ER format designer warns you about any inconsistencies between the properties of the ER format elements that refer to names that aren't included in the added Excel template.</span></span>

<span data-ttu-id="f526d-654">次の手順は、この問題がどのように発生するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-654">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="f526d-655">ER 形式コンポーネントの構成を開始します。</span><span class="sxs-lookup"><span data-stu-id="f526d-655">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="f526d-656">形式構造ツリーで、**Excel\\File** 要素 **Report** を追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-656">In the format structure tree, add the **Excel\\File** element **Report**.</span></span>
3. <span data-ttu-id="f526d-657">追加した **Excel\\File** 要素の場合、Excel ブック ファイル **A.xlsx** を添付ファイルとして追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-657">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="f526d-658">[ER パラメーター](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) で構成されているドキュメント タイプを使用して、ER 形式テンプレートのストレージを指定します。</span><span class="sxs-lookup"><span data-stu-id="f526d-658">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="f526d-659">追加した Excel ブックに名前 **ReportTitle** が含まれていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-659">Make sure that the added Excel workbook doesn't contain the name **ReportTitle**.</span></span>

4. <span data-ttu-id="f526d-660">次の **Excel\\Cell** 要素 **Title** を **Report** 要素の入れ子になった要素として追加します。</span><span class="sxs-lookup"><span data-stu-id="f526d-660">Add the following **Excel\\Cell** element **Title** as the nested element of the **Report** element.</span></span> <span data-ttu-id="f526d-661">**Excel の範囲** フィールドに、**ReportTitle** を入力します。</span><span class="sxs-lookup"><span data-stu-id="f526d-661">In the **Excel range** field, enter **ReportTitle**.</span></span>
5. <span data-ttu-id="f526d-662">**検証** を選択して、**形式デザイナー** ページで編集可能な形式コンポーネントを検査します。</span><span class="sxs-lookup"><span data-stu-id="f526d-662">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![形式デザイナー ページで入れ子になった要素とフィールドを検証する](./media/er-components-inspections-13a.png)

6. <span data-ttu-id="f526d-664">検証警告が発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-664">Notice that a validation warning occurs.</span></span> <span data-ttu-id="f526d-665">メッセージは、名前 **ReportTitle** が、使用している Excel テンプレートのシート **Sheet1** に存在しないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="f526d-665">The message states that the name **ReportTitle** doesn't exist on sheet **Sheet1** of the Excel template that you're using.</span></span>

    ![Excel テンプレートの Sheet1 に名前 ReportTitle が存在しないという検証警告](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="f526d-667">自動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-667">Automatic resolution</span></span>

<span data-ttu-id="f526d-668">この問題を自動的に修正するオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="f526d-668">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="f526d-669">手動解決</span><span class="sxs-lookup"><span data-stu-id="f526d-669">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="f526d-670">オプション 1</span><span class="sxs-lookup"><span data-stu-id="f526d-670">Option 1</span></span>

<span data-ttu-id="f526d-671">テンプレートから欠落している Excel 名を参照する要素をすべて削除して、構成済の形式を変更します。</span><span class="sxs-lookup"><span data-stu-id="f526d-671">Modify the configured format by removing all elements that refer to Excel names that are missing from the template.</span></span>

#### <a name="option-2"></a><span data-ttu-id="f526d-672">オプション 2</span><span class="sxs-lookup"><span data-stu-id="f526d-672">Option 2</span></span>

<span data-ttu-id="f526d-673">Excel テンプレートをインポートすることで、編集可能な ER 形式を [更新](er-fillable-excel.md#template-import) します。</span><span class="sxs-lookup"><span data-stu-id="f526d-673">[Update](er-fillable-excel.md#template-import) the editable ER format by importing an Excel template.</span></span> <span data-ttu-id="f526d-674">編集可能な ER 形式の構造は、インポートした ER テンプレートの構造と [同期](modify-electronic-reporting-format-reapply-excel-template.md) されます。</span><span class="sxs-lookup"><span data-stu-id="f526d-674">The structure of the editable ER format will be [synced](modify-electronic-reporting-format-reapply-excel-template.md) with the structure of the imported Excel template.</span></span>

### <a name="additional-consideration"></a><span data-ttu-id="f526d-675">その他の考慮事項</span><span class="sxs-lookup"><span data-stu-id="f526d-675">Additional consideration</span></span>

<span data-ttu-id="f526d-676">[ビジネス ドキュメント管理](er-business-document-management.md) のテンプレート エディターで ER テンプレートと形式構造を同期する方法については、[ビジネス ドキュメント テンプレートの構造の更新](er-bdm-update-structure.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f526d-676">To learn how the format structure can be synced with an ER template in the template editor of [Business document management](er-business-document-management.md), see [Update the structure of a business document template](er-bdm-update-structure.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f526d-677">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f526d-677">Additional resources</span></span>

[<span data-ttu-id="f526d-678">ALLITEMS ER 関数</span><span class="sxs-lookup"><span data-stu-id="f526d-678">ALLITEMS ER function</span></span>](er-functions-list-allitems.md)

[<span data-ttu-id="f526d-679">ALLITEMSQUERY ER 関数</span><span class="sxs-lookup"><span data-stu-id="f526d-679">ALLITEMSQUERY ER function</span></span>](er-functions-list-allitemsquery.md)

[<span data-ttu-id="f526d-680">INT64VALUE ER 関数</span><span class="sxs-lookup"><span data-stu-id="f526d-680">INT64VALUE ER function</span></span>](er-functions-conversion-int64value.md)

[<span data-ttu-id="f526d-681">INTVALUE ER 関数</span><span class="sxs-lookup"><span data-stu-id="f526d-681">INTVALUE ER function</span></span>](er-functions-conversion-intvalue.md)

[<span data-ttu-id="f526d-682">FILTER ER 関数</span><span class="sxs-lookup"><span data-stu-id="f526d-682">FILTER ER function</span></span>](er-functions-list-filter.md)

[<span data-ttu-id="f526d-683">WHERE ER 関数</span><span class="sxs-lookup"><span data-stu-id="f526d-683">WHERE ER function</span></span>](er-functions-list-where.md)

[<span data-ttu-id="f526d-684">JOIN データ ソースを使用して、ER モデル マッピングで複数のアプリケーション テーブルからデータを取得する</span><span class="sxs-lookup"><span data-stu-id="f526d-684">Use JOIN data sources to get data from multiple application tables in ER model mappings</span></span>](er-join-data-sources.md)

[<span data-ttu-id="f526d-685">電子申告形式の実行をトレースしてパフォーマンスの問題をトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="f526d-685">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="f526d-686">ビジネス ドキュメント管理の概要</span><span class="sxs-lookup"><span data-stu-id="f526d-686">Business document management overview</span></span>](er-business-document-management.md)
