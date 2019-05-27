---
title: アプリケーション オブジェクト ツリー (AOT) のテーブル プロパティ
description: このトピックでは、アプリケーション オブジェクト ツリー (AOT) におけるテーブル要素の <strong>プロパティ</strong> ウィンドウにあるプロパティについて説明します。 テーブル要素は、<strong>データ ディクショナリ</strong> &gt; <strong>テーブル</strong> にあります。
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18141
ms.assetid: 1ad8b7e9-80b3-44a3-b57d-7e9fc88db038
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: e943d52be34b95991ec31be98f362aa1c5eed84d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537234"
---
# <a name="table-properties-in-the-application-object-tree-aot"></a><span data-ttu-id="5d9b7-104">アプリケーション オブジェクト ツリー (AOT) のテーブル プロパティ</span><span class="sxs-lookup"><span data-stu-id="5d9b7-104">Table properties in the Application Object Tree (AOT)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d9b7-105">このトピックでは、アプリケーション オブジェクト ツリー (AOT) におけるテーブル要素の <strong>プロパティ</strong> ウィンドウにあるプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-105">This topic describes the properties that are in the<strong> Properties</strong> window for table elements in the Application Object Tree (AOT).</span></span> <span data-ttu-id="5d9b7-106">テーブル要素は、<strong>データ ディクショナリ</strong> &gt; <strong>テーブル</strong> にあります。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-106">Table elements are located under <strong>Data Dictionary</strong> &gt; <strong>Tables</strong>.</span></span>

<span data-ttu-id="5d9b7-107">プロパティ値の設定に関するガイドラインについては、[テーブル プロパティのベスト プラクティス](http://msdn.microsoft.com/library/5def498e-107d-4a2b-a621-fbbe0243e399(AX.60).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-107">For guidelines about setting property values, see [Best Practices for Table Properties](http://msdn.microsoft.com/library/5def498e-107d-4a2b-a621-fbbe0243e399(AX.60).aspx).</span></span> <span data-ttu-id="5d9b7-108">次は、テーブル要素の下のサブ要素になっている AOT 要素のプロパティについてのトピックの一覧です。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-108">Next is a list of topics about the properties of AOT elements that are sub-elements under a table element.</span></span>

## <a name="table-properties"></a><span data-ttu-id="5d9b7-109">表のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5d9b7-109">Table Properties</span></span>
<span data-ttu-id="5d9b7-110">次のテーブルは、AOT でのテーブル要素のプロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-110">The following table describes the properties of table elements in the AOT.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5d9b7-111">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5d9b7-111">Property</span></span></th>
<th><span data-ttu-id="5d9b7-112">説明</span><span class="sxs-lookup"><span data-stu-id="5d9b7-112">Description</span></span></th>
<th><span data-ttu-id="5d9b7-113">このバージョンの Microsoft DynamicsAX の新要素</span><span class="sxs-lookup"><span data-stu-id="5d9b7-113">New in this version of Microsoft Dynamics AX</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5d9b7-114"><strong><span class="ui">抽象</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-114"><strong><span class="ui">Abstract</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-115">テーブルが継承をサポートするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-115">Specifies whether the table supports inheritance.</span></span> <span data-ttu-id="5d9b7-116">既定値は [<span class="ui">いいえ</span>] です。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-116">The default value is <span class="ui">No</span>.</span></span> <span data-ttu-id="5d9b7-117">値が<span class="ui">はい</span>である場合、テーブルが、<span class="code">update_recordset</span>および<span class="code">select</span> ステートメントのような X++ SQL ステートメントの直接ターゲットにはなりません。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-117">If the value is <span class="ui">Yes</span>, the table cannot be a direct target of X++ SQL statements such as <span class="code">update_recordset</span> and <span class="code">select</span>.</span></span> <span data-ttu-id="5d9b7-118">このプロパティは、<span class="ui">SupportInheritance</span> プロパティが [<span class="ui">いいえ</span>] に設定されている場合は使用できません。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-118">This property is unavailable when the <span class="ui">SupportInheritance</span> property is set to <span class="ui">No</span>.</span></span> <span data-ttu-id="5d9b7-119">詳細については、「<a href="http://msdn.microsoft.com/library/cb4803e7-9a29-4c54-be43-63722557dac6(AX.60).aspx">テーブル継承の概要</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-119">For more information, see <a href="http://msdn.microsoft.com/library/cb4803e7-9a29-4c54-be43-63722557dac6(AX.60).aspx">Table Inheritance Overview</a>.</span></span></td>
<td><span data-ttu-id="5d9b7-120">AX 2012</span><span class="sxs-lookup"><span data-stu-id="5d9b7-120">AX 2012</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-121"><strong><span class="ui">AnalysisDimensionType</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-121"><strong><span class="ui">AnalysisDimensionType</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-122"><span class="ui">IsLookup</span> プロパティ設定に基づいて作成される分析コードのタイプを決定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-122">Determines the type of dimension created based on the <span class="ui">IsLookup</span> property setting.</span></span> <span data-ttu-id="5d9b7-123">次の値のいずれかを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-123">You can specify one of the following values.</span></span><ul>
<li><span data-ttu-id="5d9b7-124"><strong><span class="ui">自動</span></strong> - 表に事実データと分析コード データが含まれる可能性があることを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-124"><strong><span class="ui">Auto</span></strong> - Specifies that the table may contain factual as well as dimensional data.</span></span> <span data-ttu-id="5d9b7-125">事実に基づくデータはメジャーを作成するために抽出されますが、<strong>BI ウィザード</strong>は、分析コード データを抽出して分析コードと属性を作成します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-125">The <strong>BI Wizard</strong> will extract dimensional data and create dimensions and attributes while factual data will be extracted to create measures.</span></span> <span data-ttu-id="5d9b7-126">1 つの子分析コードが親テーブルからの属性で作成されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-126">One child dimension is created with attributes from the parent table.</span></span></li>
<li><span data-ttu-id="5d9b7-127"><strong><span class="ui">MasterInner</span></strong> - このテーブルと子テーブルの関係を作成する内部 (完全) 結合を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-127"><strong><span class="ui">MasterInner</span></strong> - Specifies an inner (full) join to create relationships with this table to the child table.</span></span> <span data-ttu-id="5d9b7-128">表およびテーブルの各レコードの組み合わせは、分析コードで生成されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-128">Each record combination for this table and the child table are generated in the dimension.</span></span> <span data-ttu-id="5d9b7-129">1 つの子分析コードが親テーブルからの属性で作成されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-129">One child dimension is created with attributes from the parent table.</span></span></li>
<li><span data-ttu-id="5d9b7-130"><strong><span class="ui">MasterLeftOuter</span></strong> - このテーブルと子テーブルの関係を作成する左外部結合を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-130"><strong><span class="ui">MasterLeftOuter</span></strong> - Specifies a left outer join to create relationships with this table to the child table.</span></span> <span data-ttu-id="5d9b7-131">分析コードには、このテーブルの値に基づいて追加の属性が設定されます。この属性は空にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-131">Dimensions will have additional attributes based on values in this table that can also be empty.</span></span> <span data-ttu-id="5d9b7-132">1 つの子分析コードが親テーブルからの属性で作成されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-132">One child dimension is created with attributes from the parent table.</span></span></li>
<li><span data-ttu-id="5d9b7-133"><strong><span class="ui">トランザクション</span></strong> - テーブルが厳密に事実データ (測定) を生成するために使用されることを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-133"><strong><span class="ui">Transaction</span></strong> - Specifies that the table should strictly be used to generate factual data (measures).</span></span> <span data-ttu-id="5d9b7-134">この設定は、テーブルにトランザクション データのみが含まれている場合に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-134">This setting should be used when a table only contains transactional data.</span></span> <span data-ttu-id="5d9b7-135">テーブルから列挙型フィールドのみを含む 1 つの子分析コードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-135">One child dimension is created containing only enumeration fields from the table.</span></span> <span data-ttu-id="5d9b7-136"><strong><span class="ui">IsLookup</span></strong> プロパティが<strong><span class="ui">いいえ</span></strong>に設定
</span><span class="sxs-lookup"><span data-stu-id="5d9b7-136"><strong><span class="ui">IsLookup</span></strong> property set to <strong><span class="ui">No</span></strong>
</span></span><li><span data-ttu-id="5d9b7-137"><strong><span class="ui">自動</span></strong> - 表に事実データと分析コード データが含まれる可能性があることを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-137"><strong><span class="ui">Auto</span></strong> - Specifies that the table may contain factual as well as dimensional data.</span></span> <span data-ttu-id="5d9b7-138">事実に基づくデータはメジャーを作成するために抽出されますが、<strong>BI ウィザード</strong>は、分析コード データを抽出して分析コードと属性を作成します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-138">The <strong>BI Wizard</strong> will extract dimensional data and create dimensions and attributes while factual data will be extracted to create measures.</span></span> <span data-ttu-id="5d9b7-139">1 つの親と子の分析コードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-139">One parent and child dimension is created.</span></span></li>
<li><span data-ttu-id="5d9b7-140"><strong><span class="ui">MasterInner</span></strong> - 適用できません。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-140"><strong><span class="ui">MasterInner</span></strong> - Not applicable.</span></span> <span data-ttu-id="5d9b7-141"><span class="ui">Auto</span> と同じ。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-141">Same as <span class="ui">Auto</span>.</span></span></li>
<li><span data-ttu-id="5d9b7-142"><strong><span class="ui">MasterLeftOuter</span></strong> - 適用できません。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-142"><strong><span class="ui">MasterLeftOuter</span></strong> - Not applicable.</span></span> <span data-ttu-id="5d9b7-143"><span class="ui">Auto</span> と同じ。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-143">Same as <span class="ui">Auto</span>.</span></span></li>
<li><span data-ttu-id="5d9b7-144"><strong><span class="ui">トランザクション</span></strong> - テーブルが厳密に事実データ (測定) を生成するために使用されることを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-144"><strong><span class="ui">Transaction</span></strong> - Specifies that the table should strictly be used to generate factual data (measures).</span></span> <span data-ttu-id="5d9b7-145">この設定は、テーブルにトランザクション データのみが含まれている場合に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-145">This setting should be used when a table only contains transactional data.</span></span> <span data-ttu-id="5d9b7-146">テーブルから列挙値のみを含む 1 つの子分析コードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-146">One child dimension is created containing only enumeration values from the table.</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-147"><strong><span class="ui">AnalysisIdentifier</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-147"><strong><span class="ui">AnalysisIdentifier</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-148">SQL Server Analysis Services (SSAS) キューブ内の分析コードの ID として使用するフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-148">Specifies the field to be used as the identifier for the dimension in a SQL Server Analysis Services (SSAS) cube.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-149"><strong><span class="ui">AOSAuthorization</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-149"><strong><span class="ui">AOSAuthorization</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-150">ユーザーのアクセス許可に応じて、ユーザーがテーブルで実行できる操作の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-150">Specifies the type of operation that a user can perform on a table, depending on the user&#39;s permissions.</span></span> <span data-ttu-id="5d9b7-151">このプロパティを <strong><span class="ui">なし</span></strong> に設定すると、承認チェックは実行されません。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-151">When the property is set to <strong><span class="ui">None</span></strong>, an authorization check is not performed.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-152"><strong><span class="ui">CacheLookup</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-152"><strong><span class="ui">CacheLookup</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-153">ルックアップ操作中に取得されたレコードをキャッシュする方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-153">Determines how to cache the records retrieved during a lookup operation.</span></span> <span data-ttu-id="5d9b7-154">この <strong><span class="ui">CacheLookup</span></strong> プロパティは、別のテーブルから継承しないテーブルのみに存在します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-154">This <strong><span class="ui">CacheLookup</span></strong> property exists only on tables that do not inherit from another table.</span></span> <span data-ttu-id="5d9b7-155">継承ルート テーブルでは、AOT <span class="ui">プロパティ</span>ウィンドウを使用して、このプロパティを <strong><span class="ui">EntireTable</span></strong> に設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-155">On an inheritance root table, this property cannot be set to <strong><span class="ui">EntireTable</span></strong> by using the AOT <span class="ui">Properties</span> window.</span></span> <span data-ttu-id="5d9b7-156">継承ルート テーブルにこの値を割り当てるために、他の手法を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-156">You must not use other techniques to assign this value to inheritance root tables.</span></span> <span data-ttu-id="5d9b7-157">たとえば、この値を割り当てる <strong><span class="code">TreeNode</span></strong> クラスの <strong><span class="code">AOTsetProperty</span></strong> メソッドを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-157">For example, do not use the <strong><span class="code">AOTsetProperty</span></strong> method of the <strong><span class="code">TreeNode</span></strong> class to assign this value.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-158"><strong><span class="ui">ClusterIndex</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-158"><strong><span class="ui">ClusterIndex</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-159">クラスター インデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-159">Specifies the cluster index.</span></span> <span data-ttu-id="5d9b7-160">このプロパティは、SQL 最適化の目的でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-160">This property is used only for SQL optimization purposes.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-161"><strong><span class="ui">ConfigurationKey</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-161"><strong><span class="ui">ConfigurationKey</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-162">テーブルのコンフィギュレーション キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-162">Specifies the configuration key for the table.</span></span> <span data-ttu-id="5d9b7-163">コンフィギュレーション キーにより、システム管理者はアプリケーションの特定の部分を有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-163">Configuration keys allow a system administrator to enable and disable certain parts of an application.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-164"><strong><span class="ui">CountryRegionCodes</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-164"><strong><span class="ui">CountryRegionCodes</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-165">テーブルが適用されるか有効な国/地域コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-165">Specifies the country region codes where the table is applicable or valid.</span></span> <span data-ttu-id="5d9b7-166">クライアント フレームワークおよびアプリケーションは、このプロパティを使用して、国または地域固有の機能を有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-166">The client framework and application may make use of this property to enable or disable country or region specific features.</span></span> <span data-ttu-id="5d9b7-167">これは、カンマで区切られた単一の文字列の ISO コードのリストとして実装されています。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-167">This is implemented as a comma-separated list of ISO country codes in a single string.</span></span> <span data-ttu-id="5d9b7-168">値は、グローバル アドレス帳に含まれるデータと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-168">The values must match data contained in the global address book.</span></span></td>
<td><span data-ttu-id="5d9b7-169">AX 2012</span><span class="sxs-lookup"><span data-stu-id="5d9b7-169">AX 2012</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-170"><strong><span class="ui">CountryRegionContextField</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-170"><strong><span class="ui">CountryRegionContextField</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-171">国のコンテキストを識別するために使用されるフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-171">Specifies the field that will be used to identify the country context.</span></span> <span data-ttu-id="5d9b7-172">これは<strong><span class="ui">CountryRegionCodes</span></strong> プロパティに関連しています。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-172">This relates to the <strong><span class="ui">CountryRegionCodes</span></strong> property.</span></span></td>
<td><span data-ttu-id="5d9b7-173">AX 2012</span><span class="sxs-lookup"><span data-stu-id="5d9b7-173">AX 2012</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-174"><strong><span class="ui">CreatedBy</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-174"><strong><span class="ui">CreatedBy</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-175">システムがテーブルのレコードの <strong><span class="code">CreatedBy</span></strong> フィールドを管理しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-175">Indicates whether the system maintains the <strong><span class="code">CreatedBy</span></strong> field for the records in a table.</span></span> <span data-ttu-id="5d9b7-176">このフィールドには、特定のレコードの作成者に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-176">This field contains information about who created a particular record.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-177"><strong><span class="ui">CreatedDateTime</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-177"><strong><span class="ui">CreatedDateTime</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-178">システムがテーブルのレコードの <strong><span class="code">CreationDate</span></strong> および <strong><span class="ui">CreationTime</span></strong> フィールドを管理しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-178">Indicates whether the system maintains the <strong><span class="code">CreationDate</span></strong> and <strong><span class="ui">CreationTime</span></strong> fields for the records in a table.</span></span> <span data-ttu-id="5d9b7-179">このフィールドには、レコードが最後に作成された日付が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-179">This field contains the date when a record was created.</span></span></td>
<td><span data-ttu-id="5d9b7-180">AX 2012</span><span class="sxs-lookup"><span data-stu-id="5d9b7-180">AX 2012</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-181"><strong><span class="ui">CreatedTransactionId</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-181"><strong><span class="ui">CreatedTransactionId</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-182">システムがテーブルのレコードの <strong><span class="code">CreatedTransactionId</span></strong> フィールドを管理しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-182">Indicates whether the system maintains the <strong><span class="code">CreatedTransactionId</span></strong> field for the records in a table.</span></span> <span data-ttu-id="5d9b7-183">このフィールドにはレコードを作成した取引に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-183">This field contains information about which transaction created the record.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-184"><strong><span class="ui">CreateRecIdIndex</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-184"><strong><span class="ui">CreateRecIdIndex</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-185"><strong>レコード ID</strong> フィールドでインデックスが作成されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-185">Indicates whether an index on the <strong>Record ID</strong> field is created.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-186"><strong><span class="ui">DeveloperDocumentation</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-186"><strong><span class="ui">DeveloperDocumentation</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-187">テーブルの目的を説明し、アプリケーションでどのように使用されるかを説明します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-187">Describes the purpose of a table and explains how it is used in the application.</span></span> <span data-ttu-id="5d9b7-188">説明は、通常 5 つ以下の構文で構成され、単一の段落として書かれます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-188">A description is typically no more than five sentences long and is written as a single paragraph.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-189"><strong><span class="ui">EntityRelationshipType</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-189"><strong><span class="ui">EntityRelationshipType</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-190">共通エンティティ リレーションシップ (ER) データ モデルの表記法に従ってテーブルを分類します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-190">Classifies a table according to common entity relationship (ER) data model notation.</span></span> <span data-ttu-id="5d9b7-191">テーブルは、エンティティまたはリレーションシップとして分類されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-191">A table is classified as an entity or a relationship.</span></span> <span data-ttu-id="5d9b7-192">エンティティはオブジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-192">An entity represents an object.</span></span> <span data-ttu-id="5d9b7-193">リレーションシップは、2 つのオブジェクトの間の関連付けを表します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-193">A relationship represents an association between two objects.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-194"><strong><span class="ui">拡張</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-194"><strong><span class="ui">Extends</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-195">プロパティ値として選択された別のテーブルからテーブルを派生させます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-195">Derives the table from another table that is chosen as the property value.</span></span> <span data-ttu-id="5d9b7-196"><span class="ui">SupportInheritance</span> プロパティが <span class="ui">Yes</span> に設定されている場合、値は null です。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-196">The value is null when the <span class="ui">SupportInheritance</span> property is set to <span class="ui">Yes</span>.</span></span> <span data-ttu-id="5d9b7-197">詳細については、「<a href="http://msdn.microsoft.com/library/cb4803e7-9a29-4c54-be43-63722557dac6(AX.60).aspx">テーブル継承の概要</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-197">For more information, see <a href="http://msdn.microsoft.com/library/cb4803e7-9a29-4c54-be43-63722557dac6(AX.60).aspx">Table Inheritance Overview</a>.</span></span></td>
<td><span data-ttu-id="5d9b7-198">AX 2012</span><span class="sxs-lookup"><span data-stu-id="5d9b7-198">AX 2012</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-199"><strong><span class="ui">FormRef</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-199"><strong><span class="ui">FormRef</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-200">テーブルが参照されているときに発生する表示メニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-200">Specifies the display menu item that is activated when a table is referenced.</span></span> <span data-ttu-id="5d9b7-201">表示メニュー項目は、フォームに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-201">A display menu item is associated with a form.</span></span> <span data-ttu-id="5d9b7-202">レポートのプライマリ インデックス フィールドを使用するとき、このフォームはレポート内のリンクとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-202">When you use a primary index field on a report, this form is available as a link in the report.</span></span> <span data-ttu-id="5d9b7-203">プライマリ インデックスを指定するには、<strong><span class="code">PrimaryIndex</span></strong> プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-203">A primary index is specified by using the <strong><span class="code">PrimaryIndex</span></strong> property.</span></span> <span data-ttu-id="5d9b7-204">このフィールドを空白のままにすると、システムではでテーブルと同じ名前のフォームを表示しようとします。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-204">If you leave this field blank, the system attempts to display a form that has the same name as the table.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-205"><strong><span class="ui">ID</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-205"><strong><span class="ui">ID</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-206">システムによって生成されたテーブル <span class="code">ID</span> を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-206">Specifies the table <span class="code">ID</span> generated by the system.</span></span> <span data-ttu-id="5d9b7-207">詳細については、「<a href="http://msdn.microsoft.com/library/2951f194-4362-460e-8607-7f9fc0022449(AX.60).aspx">アプリケーション オブジェクト ID</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-207">For more information, see <a href="http://msdn.microsoft.com/library/2951f194-4362-460e-8607-7f9fc0022449(AX.60).aspx">Application Object IDs</a>.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-208"><strong><span class="ui">IsLookup</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-208"><strong><span class="ui">IsLookup</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-209">レポート モデルについては、テーブルの情報が、レポート モデルが生成されるときに参照する他のテーブルに組み込まれているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-209">For report models, it specifies whether the table information is incorporated into other tables that reference it when a report model is generated.</span></span> <span data-ttu-id="5d9b7-210">OLAP キューブで、連結分析コードまたは異なる分析コードを生成するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-210">For OLAP cubes, it determines whether to generate a consolidated dimension or a distinct dimension.</span></span> <span data-ttu-id="5d9b7-211">次の値のいずれかを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-211">You can specify one of the following values.</span></span>
<ul>
<li><span data-ttu-id="5d9b7-212"><strong><span class="ui">はい</span></strong> - テーブルの属性が親分析コード (スター スキーマ) に連結されることを示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-212"><strong><span class="ui">Yes</span></strong> - Indicates that attributes from the table are to be consolidated into the parent dimension (star schema).</span></span></li>
<li><span data-ttu-id="5d9b7-213"><strong><span class="ui">いいえ</span></strong> - テーブル (スノーフレーク スキーマ) に対して個別の分析コードが生成されることを示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-213"><strong><span class="ui">No</span></strong> - Indicates that a separate dimension is to be generated for the table (snowflake schema).</span></span></li>
</ul>
<span data-ttu-id="5d9b7-214">分析コードおよびスターとスノーフレーク スキーマの詳細については、<a href="http://go.microsoft.com/fwlink/?LinkId=115450">分析コードの概要 (SQL Server 2005 オンライン ブック)</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-214">For more information about dimensions and star and snowflake schemas, see <a href="http://go.microsoft.com/fwlink/?LinkId=115450">Introduction to Dimensions (SQL Server 2005 Books Online)</a>.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-215"><strong><span class="ui">ラベル</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-215"><strong><span class="ui">Label</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-216">テーブルのラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-216">Specifies the label for a table.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-217"><strong><span class="ui">ListPageRef</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-217"><strong><span class="ui">ListPageRef</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-218">このレコードの種類の一覧を表示できるフォームをポイントする表示メニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-218">Specifies a display menu item that points to a form that can show a list of this record type.</span></span></td>
<td><span data-ttu-id="5d9b7-219">AX 2012</span><span class="sxs-lookup"><span data-stu-id="5d9b7-219">AX 2012</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-220"><strong><span class="ui">モデル</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-220"><strong><span class="ui">Model</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-221">テーブルがあるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-221">Specifies which model the table is in.</span></span> <span data-ttu-id="5d9b7-222">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-222">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="5d9b7-223">要素は、レイヤー内の 1 つのモデルに正確に存在します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-223">An element can exist in exactly one model in a layer.</span></span> <span data-ttu-id="5d9b7-224">要素例には、テーブルまたはクラスがあります。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-224">Examples of elements are a table or class.</span></span> <span data-ttu-id="5d9b7-225">上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-225">The same element can exist in a customized version in a model in a higher layer.</span></span></td>
<td><span data-ttu-id="5d9b7-226">AX 2012</span><span class="sxs-lookup"><span data-stu-id="5d9b7-226">AX 2012</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-227"><strong><span class="ui">ModifiedBy</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-227"><strong><span class="ui">ModifiedBy</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-228">システムがテーブルのレコードの <strong><span class="code">ModifiedBy</span></strong> フィールドを管理しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-228">Indicates whether the system maintains the <strong><span class="code">ModifiedBy</span></strong> field for the records in a table.</span></span> <span data-ttu-id="5d9b7-229">このフィールドは、レコードに最後の変更を行った人を記録します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-229">This field records the person who performed the last modification to a record.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-230"><strong><span class="ui">ModifiedDateTime</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-230"><strong><span class="ui">ModifiedDateTime</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-231">システムがテーブルのレコードの <strong><span class="code">ModifiedDateTime</span></strong> フィールドを管理しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-231">Indicates whether the system maintains the <strong><span class="code">ModifiedDateTime</span></strong> field for the records in a table.</span></span> <span data-ttu-id="5d9b7-232">このフィールドには、レコードの最終変更日が記録されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-232">This field records the date of the last modification of a record.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-233"><strong><span class="ui">ModifiedTime</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-233"><strong><span class="ui">ModifiedTime</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-234">システムがテーブルのレコードの <strong><span class="code">ModifiedTime</span></strong> フィールドを管理しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-234">Indicates whether the system maintains the <strong><span class="code">ModifiedTime</span></strong> field for the records in a table.</span></span> <span data-ttu-id="5d9b7-235">このフィールドには、レコードが最後に変更された時刻が記録されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-235">This field records the time when a record was last modified.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-236"><strong><span class="ui">名前</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-236"><strong><span class="ui">Name</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-237">テーブル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-237">Specifies the table name.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-238"><strong><span class="ui">OccEnabled</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-238"><strong><span class="ui">OccEnabled</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-239">テーブルでオプティミスティック同時実行モードを有効にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-239">Specifies whether the optimistic concurrency mode is enabled for a table.</span></span> <span data-ttu-id="5d9b7-240">このモードを有効にすると、データがデータベースからフェッチされるときに、データは今後の変更からロックされません。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-240">When this mode is enabled, data is not locked from future modification when it is fetched from the database.</span></span> <span data-ttu-id="5d9b7-241">データは、実際の更新の実行時にのみロックされます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-241">Data is locked only when the actual update is performed.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-242"><strong><span class="ui">PreviewPartRef</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-242"><strong><span class="ui">PreviewPartRef</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-243">拡張プレビューで使用される<span class="ui">情報パーツ</span>または<span class="ui">フォーム パーツ</span>を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-243">Specifies the <span class="ui">Info Part</span> or <span class="ui">Form Part</span> to be used in the enhanced preview.</span></span> <span data-ttu-id="5d9b7-244">情報パーツは指定したクエリからデータ フィールドのコレクションを表示しています。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-244">An info part shows a collection of data fields from a specified query.</span></span> <span data-ttu-id="5d9b7-245">情報パーツはメタデータを使用してデータの表示方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-245">An info part uses metadata to describe how the data appears.</span></span> <span data-ttu-id="5d9b7-246">フォーム パーツは、フォームへのポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-246">A form part represents a pointer to a form.</span></span></td>
<td><span data-ttu-id="5d9b7-247">AX 2012</span><span class="sxs-lookup"><span data-stu-id="5d9b7-247">AX 2012</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-248"><strong><span class="ui">PrimaryIndex</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-248"><strong><span class="ui">PrimaryIndex</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-249">プライマリ インデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-249">Specifies the primary index.</span></span> <span data-ttu-id="5d9b7-250">固有のインデックスのみ選択することができます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-250">Only a unique index can be selected.</span></span> <span data-ttu-id="5d9b7-251">このプロパティは、データベースの最適化を目的として、またキャッシュ キーとして使用するユニーク索引を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-251">The property is used for database optimization purposes and to indicate which unique index to use as the caching key.</span></span> <span data-ttu-id="5d9b7-252">プライマリ インデックスが指定されていない場合、最下位の ID の固有のインデックスは、キャッシュ キーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-252">If a primary index is not specified, the unique index with the lowest ID is used as the caching key.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-253"><strong><span class="ui">ReplacementKey</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-253"><strong><span class="ui">ReplacementKey</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-254">一部のフォーム コントロール内のデータの識別子として表示するフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-254">Specifies the fields to display as the identifier for data in some form controls.</span></span></td>
<td><span data-ttu-id="5d9b7-255">AX 2012</span><span class="sxs-lookup"><span data-stu-id="5d9b7-255">AX 2012</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-256"><strong><span class="ui">ReportRef</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-256"><strong><span class="ui">ReportRef</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-257">テーブルが参照されているときに発生する出力メニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-257">Specifies the output menu item that is activated when a table is referenced.</span></span> <span data-ttu-id="5d9b7-258">出力メニュー項目はレポートに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-258">An output menu item is associated with a report.</span></span> <span data-ttu-id="5d9b7-259">レポートのプライマリ インデックス フィールドを使用するとき、このレポートはレポート内のリンクとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-259">When you use a primary index field on a report, this report is available as a link in the report.</span></span> <span data-ttu-id="5d9b7-260">プライマリ インデックスを指定するには、<span class="code">PrimaryIndex</span> プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-260">A primary index is specified using the <span class="code">PrimaryIndex</span> property.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-261"><strong><span class="ui">SaveDataPerCompany</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-261"><strong><span class="ui">SaveDataPerCompany</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-262">現在の会社のデータが保存されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-262">Indicates whether the data for the current company is saved.</span></span> <span data-ttu-id="5d9b7-263">プロパティを<strong><span class="ui">いいえ</span></strong>に設定すると、データは会社識別子 (<span class="code">DataAreaId</span>) なしで保存されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-263">If you set the property to<strong><span class="ui"> No</span></strong>, data is saved without a company identifier (<span class="code">DataAreaId</span>).</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5d9b7-264"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-264"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5d9b7-265"><strong><span class="code">SaveDataPerCompany</span></strong> プロパティが<strong>はい</strong>に設定されている場合、テーブルをデータ ソースとして使用するフォーム デザインの <strong><span class="code">SetCompany</span></strong> プロパティもはいに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-265">If the <strong><span class="code">SaveDataPerCompany</span></strong> property on a table is set to <strong>Yes</strong>, the <strong><span class="code">SetCompany</span></strong> property on a form design that uses the table as a data source must also be set to Yes.</span></span></td>
</tr>
</tbody>
</table>
</div>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5d9b7-266"><strong>ヒント</strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-266"><strong>Tip</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5d9b7-267">会社の略語はステータス行に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-267">The company acronym can be seen in the status line.</span></span> <span data-ttu-id="5d9b7-268">略称をダブルクリックするとダイアログ ボックスが開き、別の会社に変更されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-268">Double-clicking the acronym opens a dialog box to change to another company.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-269"><strong><span class="ui">SaveDataPerPartition</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-269"><strong><span class="ui">SaveDataPerPartition</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-270">テーブルに <strong><span class="code">Partition</span></strong> という名前のシステム フィールドが含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-270">Shows whether the table has a system field named <strong><span class="code">Partition</span></strong>.</span></span> <span data-ttu-id="5d9b7-271">これは、読み取り専用のシステム フィールドを意味します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-271">This is meant to be a read-only system field.</span></span> <span data-ttu-id="5d9b7-272">テーブルに<strong><span class="code">パーティション</span></strong> フィールドがない場合、各レコードに 1 つのパーティションに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-272">If the table has a <strong><span class="code">Partition</span></strong> field, each record is assigned to one partition.</span></span> <span data-ttu-id="5d9b7-273">各レコードは、他のパーティションのコンテキストで実行されるデータ アクセス操作から隠されています。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-273">Each record is kept hidden from data access operations that are run under the context of other partitions.</span></span></td>
<td><span data-ttu-id="5d9b7-274">AX 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5d9b7-274">AX 2012 R2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-275"><strong><span class="ui">SearchLinkRefName</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-275"><strong><span class="ui">SearchLinkRefName</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-276">エンタープライズ ポータルの検索結果に表示されるテーブル レコードに関する Web サイトの情報にリンクするメニュー項目の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-276">Specifies the name of the menu item that links to information on a Web site about a table record listed in the Enterprise Portal search results.</span></span> <span data-ttu-id="5d9b7-277"><strong><span class="code">SearchLinkRefType</span></strong> プロパティが URL に設定されている場合、メニュー項目を、テーブル データが表示されている Web パーツ ページにリンクする <strong><span class="code">SearchLinkRefName</span></strong> プロパティ リストから選択します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-277">If the <strong><span class="code">SearchLinkRefType</span></strong> property is set to URL, select a menu item from the <strong><span class="code">SearchLinkRefName</span></strong> property list that links to a Web part page that displays the table data.</span></span> <span data-ttu-id="5d9b7-278">Web パーツ ページのフォームおよびレポートは、データを表示できます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-278">Forms and reports on Web part pages can display data.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-279"><strong><span class="ui">SearchLinkRefType</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-279"><strong><span class="ui">SearchLinkRefType</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-280">エンタープライズ ポータルの検索結果に表示されるテーブル レコードに関する Web サイトの情報にリンクするメニュー項目のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-280">Specifies the type of the menu item that links to information on a Web site about a table record listed in the Enterprise Portal search results.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-281"><strong><span class="ui">SingularLabel</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-281"><strong><span class="ui">SingularLabel</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-282">テーブルに格納される品目の 1 つの名前を表示するために、レポート モデルまたはキューブで使用されるラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-282">Specifies the label that is used in a report model or a cube to display the singular name of items stored in the table.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-283"><strong><span class="ui">SupportInheritance</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-283"><strong><span class="ui">SupportInheritance</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-284">このプロパティを <strong><span class="ui">Yes</span></strong> に設定ｓるうと、<strong><span class="ui">Extends</span></strong> や <strong><span class="ui">Abstract</span></strong> などの、その他の継承関連のプロパティの値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-284">Setting this property to <strong><span class="ui">Yes</span></strong> enables you to set a value for other inheritance related properties such as <strong><span class="ui">Extends</span></strong> and <strong><span class="ui">Abstract</span></strong>.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5d9b7-285"><strong>注意 </strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-285"><strong>Caution</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5d9b7-286">値を<strong><span class="ui">はい</span></strong>に設定するとき、テーブル上のどのフィールドも削除され、再度作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-286">When you set the value to <strong><span class="ui">Yes</span></strong>, any fields on the table are dropped and must be created again.</span></span></td>
</tr>
</tbody>
</table>
</div>
<span data-ttu-id="5d9b7-287">詳細については、「<a href="http://msdn.microsoft.com/library/cb4803e7-9a29-4c54-be43-63722557dac6(AX.60).aspx">テーブル継承の概要</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-287">For more information, see <a href="http://msdn.microsoft.com/library/cb4803e7-9a29-4c54-be43-63722557dac6(AX.60).aspx">Table Inheritance Overview</a>.</span></span></td>
<td><span data-ttu-id="5d9b7-288">AX 2012</span><span class="sxs-lookup"><span data-stu-id="5d9b7-288">AX 2012</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-289"><strong><span class="ui">SystemTable</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-289"><strong><span class="ui">SystemTable</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-290">テーブルをシステム テーブルとして表示するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-290">Indicates if a table appears as a System table.</span></span> <span data-ttu-id="5d9b7-291">エクスポートおよびインポート中にフィルターできます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-291">It can then be filtered during export and import.</span></span> <span data-ttu-id="5d9b7-292">システム テーブルは、ログイン時に常に同期されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-292">System tables are always synchronized when you log in.</span></span> <span data-ttu-id="5d9b7-293">これは、ログインするとすぐに使用するテーブルに便利です。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-293">This may be useful for tables that you use as soon as you log in.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-294"><strong><span class="ui">TableContents</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-294"><strong><span class="ui">TableContents</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-295">顧客間でセットアップ/パラメーター データを再利用する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-295">Specifies how setup/parameter data can be reused from one customer to another.</span></span> <span data-ttu-id="5d9b7-296">次の値が可能です。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-296">The following values are possible:</span></span>
<ul>
<li><span data-ttu-id="5d9b7-297"><strong><span class="ui">指定なし</span></strong> - ほとんどのテーブルで。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-297"><strong><span class="ui">Not specified</span></strong> – For most tables.</span></span></li>
<li><span data-ttu-id="5d9b7-298"><strong><span class="ui">既定のデータ</span></strong> - 郵便番号、単位、時間間隔などの顧客に依存しないデータに使用します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-298"><strong><span class="ui">Default Data</span></strong> – Use for customer-independent data such as ZIP/Postal Codes, units, and time intervals.</span></span></li>
<li><span data-ttu-id="5d9b7-299"><strong><span class="ui">基本データ</span></strong> - カレンダー、グループ、およびパラメータなどの顧客に依存するデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-299"><strong><span class="ui">Base Data</span></strong> – Use for customer-dependent data such as calendars, groups, and parameters.</span></span></li>
<li><span data-ttu-id="5d9b7-300"><strong><span class="ui">既定 + 基本データ</span></strong> - ローカル知覚が異なるデータに使用します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-300"><strong><span class="ui">Default+Base data</span></strong> – Use for data where the local perception varies.</span></span> <span data-ttu-id="5d9b7-301">たとえば、勘定科目表は、ドイツでは顧客に依存していませんが、世界の他のほとんどの場所では顧客に依存しています。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-301">For example, Chart of Accounts is not customer-dependent in Germany, but is most other places in the world.</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-302"><strong><span class="ui">TableGroup</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-302"><strong><span class="ui">TableGroup</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-303">テーブルが属するグループを決定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-303">Determines which group the table belongs to.</span></span> <span data-ttu-id="5d9b7-304"><a href="http://msdn.microsoft.com/library/3330d438-ab53-44db-9a9b-a044ed19608d(AX.60).aspx">テーブル グループ</a>は、テーブルに含まれるデータのタイプに応じてテーブルを分類する方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-304"><a href="http://msdn.microsoft.com/library/3330d438-ab53-44db-9a9b-a044ed19608d(AX.60).aspx">Table Groups</a> provide a method for categorizing tables according to the type of data they contain.</span></span> <span data-ttu-id="5d9b7-305">テーブルをデータ ソースとして使用することにより、フォーム内のテーブルから更新または削除するときにシステムがユーザーに確認を求めるかどうか定義するためにテーブル グループを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-305">Table groups can be used to define whether the system should prompt users when they update or delete from the table in forms by using the table as the data source.</span></span> <span data-ttu-id="5d9b7-306">データをエクスポートするとき、テーブル グループを使用してレコードをフィルターすることができます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-306">When exporting data, you can use table groups to filter records.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-307"><strong><span class="ui">TableType</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-307"><strong><span class="ui">TableType</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-308">Microsoft Dynamics AX 2009 にある <strong><span class="ui">一時的な</span></strong> プロパティを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-308">Replaces the <strong><span class="ui">Temporary</span></strong> property found in Microsoft Dynamics AX 2009.</span></span> <span data-ttu-id="5d9b7-309">詳細については、<a href="http://msdn.microsoft.com/library/9986b514-6079-499a-b491-9a95589f8229(AX.60).aspx">一時テーブルおよび TableType プロパティ</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-309">For more information, see <a href="http://msdn.microsoft.com/library/9986b514-6079-499a-b491-9a95589f8229(AX.60).aspx">Temporary Tables and the TableType Property</a>.</span></span></td>
<td><span data-ttu-id="5d9b7-310">AX 2012</span><span class="sxs-lookup"><span data-stu-id="5d9b7-310">AX 2012</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-311"><strong><span class="ui">TitleField1</span></strong>, <strong><span class="ui">TitleField2</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-311"><strong><span class="ui">TitleField1</span></strong>, <strong><span class="ui">TitleField2</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-312">次の操作を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-312">Enables you to do the following:</span></span>
<ul>
<li><span data-ttu-id="5d9b7-313">フォーム キャプションにテーブル フィールド データを追加します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-313">Add table field data to a form caption.</span></span></li>
<li><span data-ttu-id="5d9b7-314">ルックアップ フォームに追加のフィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-314">Display additional fields in a lookup form.</span></span> <span data-ttu-id="5d9b7-315">詳細については、<a href="http://msdn.microsoft.com/library/2e365e4b-842a-44eb-b0fa-6fa4c8c1e0fe(AX.60).aspx">方法: ルックアップ フォームでコントロールの追加</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-315">For more information, see <a href="http://msdn.microsoft.com/library/2e365e4b-842a-44eb-b0fa-6fa4c8c1e0fe(AX.60).aspx">How to: Add a Control with a Lookup Form</a>.</span></span> <span data-ttu-id="5d9b7-316"><strong><span class="code">TitleField1</span></strong> プロパティは、フォーム上のフィールドでルックアップ リストを有効化するときにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-316">The <strong><span class="code">TitleField1</span></strong> property is also used when activating the lookup list in a field on a form.</span></span> <span data-ttu-id="5d9b7-317"><strong><span class="code">TitleField1</span></strong> および <strong><span class="code">TitleField2</span></strong> プロパティに指定するフィールドはキー値でマージすることができます</span><span class="sxs-lookup"><span data-stu-id="5d9b7-317">The fields you specify for <strong><span class="code">TitleField1</span></strong> and <strong><span class="code">TitleField2</span></strong> properties can be merged with the key value.</span></span></li>
<li><span data-ttu-id="5d9b7-318">ツールヒントにフィールドの情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-318">Display field information in a tooltip.</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-319"><strong><span class="ui">TypicalRowCount</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-319"><strong><span class="ui">TypicalRowCount</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-320">テーブル内に通常表示されるレコード数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-320">Specifies the number of records that typically appear in a table.</span></span> <span data-ttu-id="5d9b7-321"><strong><span class="code">AnalysisSelection</span></strong> プロパティが設定されていない場合は、<strong><span class="code">TypicalRowCount</span></strong> プロパティは、Microsoft SQL Server Reporting Services 用のレポート ビルダーを使用してレコードを選択する方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-321">If the <strong><span class="code">AnalysisSelection</span></strong> property is not set, the <strong><span class="code">TypicalRowCount</span></strong> property determines how records are selected by using Report Builder for Microsoft SQL Server Reporting Services.</span></span> <span data-ttu-id="5d9b7-322"><strong><span class="code">TypicalRowCount</span></strong> プロパティの設定は、ドロップダウン リスト、リスト ボックス、フィルタリングされたリスト ボックスを使用してテーブル レコードを選択するかどうかに影響します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-322">The <strong><span class="code">TypicalRowCount</span></strong> property setting affects whether a drop-down list, list box, or a filtered list box is used to select table records.</span></span> <span data-ttu-id="5d9b7-323">詳細については、<a href="http://msdn.microsoft.com/library/5def498e-107d-4a2b-a621-fbbe0243e399(AX.60).aspx">テーブル プロパティのベスト プラクティス</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-323">For more information, see <a href="http://msdn.microsoft.com/library/5def498e-107d-4a2b-a621-fbbe0243e399(AX.60).aspx">Best Practices for Table Properties</a>.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d9b7-324"><strong><span class="ui">ValidTimeStateFieldType</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-324"><strong><span class="ui">ValidTimeStateFieldType</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-325">期間内のデータを追跡するときに使用するためのシステムの日付/時刻フィールドのタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-325">Specifies the type of date-time field for the system to use when it tracks data within time spans.</span></span></td>
<td><span data-ttu-id="5d9b7-326">AX 2012</span><span class="sxs-lookup"><span data-stu-id="5d9b7-326">AX 2012</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d9b7-327"><strong><span class="ui">表示</span></strong></span><span class="sxs-lookup"><span data-stu-id="5d9b7-327"><strong><span class="ui">Visible</span></strong></span></span></td>
<td><span data-ttu-id="5d9b7-328">テーブルがフォームやレポート内のデータ ソースとして使用される場合のアクセス権を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-328">Specifies the access rights when the table is used as a data source in a form or a report.</span></span> <span data-ttu-id="5d9b7-329">テーブルをフォーム内のデータ ソースとして使用する場合、フォームのアクセス権は、テーブルに対して定義されているアクセス権を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-329">If the table is used as a data source in a form, then the access rights in the form cannot exceed the access rights defined for the table.</span></span></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="tables-and-report-models"></a><span data-ttu-id="5d9b7-330">テーブルおよびレポート モデル</span><span class="sxs-lookup"><span data-stu-id="5d9b7-330">Tables and Report Models</span></span>
<span data-ttu-id="5d9b7-331">次のプロパティは、レポートに情報を追加するために使用されるレポート モデルに関連しています。</span><span class="sxs-lookup"><span data-stu-id="5d9b7-331">The following properties are related to report models that are used to add information to a report.</span></span>
-   <span data-ttu-id="5d9b7-332">AnalysisSelection</span><span class="sxs-lookup"><span data-stu-id="5d9b7-332">AnalysisSelection</span></span>
-   <span data-ttu-id="5d9b7-333">AnalysisVisibility</span><span class="sxs-lookup"><span data-stu-id="5d9b7-333">AnalysisVisibility</span></span>
-   <span data-ttu-id="5d9b7-334">IsLookup</span><span class="sxs-lookup"><span data-stu-id="5d9b7-334">IsLookup</span></span>
-   <span data-ttu-id="5d9b7-335">SingularLabel</span><span class="sxs-lookup"><span data-stu-id="5d9b7-335">SingularLabel</span></span>
-   <span data-ttu-id="5d9b7-336">TypicalRowCount</span><span class="sxs-lookup"><span data-stu-id="5d9b7-336">TypicalRowCount</span></span>



<a name="additional-resources"></a><span data-ttu-id="5d9b7-337">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="5d9b7-337">Additional resources</span></span>
--------

<span data-ttu-id="5d9b7-338">[AOT のデータ ディクショナリ ノード](http://msdn.microsoft.com/library/4d7d1f77-11b8-4d8a-a44c-85e7d288c368(AX.60).aspx)</span><span class="sxs-lookup"><span data-stu-id="5d9b7-338">[Data Dictionary Node in the AOT](http://msdn.microsoft.com/library/4d7d1f77-11b8-4d8a-a44c-85e7d288c368(AX.60).aspx)</span></span>



