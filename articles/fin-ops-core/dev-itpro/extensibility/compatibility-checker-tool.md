---
title: 互換性チェック ツール
description: このトピックでは、メタデータの互換性を破る変更を検索して報告する互換性チェックツールについて説明します。
author: smithanataraj
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2020-03-26
ms.dyn365.ops.version: Platform update 34
ms.openlocfilehash: 38bad607ce8a5241b2cfb89f1fd53c803eae6707
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409266"
---
# <a name="compatibility-checker-tool"></a><span data-ttu-id="91ca8-103">互換性チェック ツール</span><span class="sxs-lookup"><span data-stu-id="91ca8-103">Compatibility checker tool</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91ca8-104">互換性チェックツールを使用すると、指定されたベースライ ンリリースまたは更新に対して、メタデータの互換性に影響する変更を検出できます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-104">The compatibility checker tool can detect metadata breaking changes against a specified baseline release or update.</span></span> <span data-ttu-id="91ca8-105">このように下位互換性を確保します。</span><span class="sxs-lookup"><span data-stu-id="91ca8-105">In this way, it helps ensure backward compatibility.</span></span> <span data-ttu-id="91ca8-106">Microsoft では、メタデータの互換性確保にこのツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="91ca8-106">Microsoft uses the tool to help ensure metadata compatibility.</span></span>

<span data-ttu-id="91ca8-107">互換性チェックツールは、プラットフォーム更新プログラム 34 の開発ツールの 1 つとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-107">The compatibility checker tool is available as one of the dev tools in Platform update 34.</span></span> <span data-ttu-id="91ca8-108">この方法を使用すると、更新プログラムを顧客にインストール、プッシュ配信する前に、ソリューションに旧版のリリースとの下位互換性を持たせることができます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-108">You can use it to ensure that your solutions are backward-compatible with earlier releases before you install or push updates to customers.</span></span>

## <a name="what-the-tool-detects"></a><span data-ttu-id="91ca8-109">ツールによって検出される内容</span><span class="sxs-lookup"><span data-stu-id="91ca8-109">What the tool detects</span></span>

<span data-ttu-id="91ca8-110">このツールでは、現在のバージョンのメタデータとベースライン バージョンのメタデータが比較されます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-110">The tool compares metadata of the current version with metadata of a baseline version.</span></span> <span data-ttu-id="91ca8-111">Microsoft が破損を判断してツールに追加したメタデータの変更を検出して報告します。</span><span class="sxs-lookup"><span data-stu-id="91ca8-111">It detects and reports metadata changes that Microsoft has identified as breaking and added to the tool.</span></span>

<span data-ttu-id="91ca8-112">ツールが検出する互換性を破る変更のリストについては、このトピックで後述する[ツールが検出する互換性を破る変更のリスト](#list-of-breaking-changes-detected-by-the-tool)のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="91ca8-112">For a list of breaking changes that the tool detects, see the [List of breaking changes detected by the tool](#list-of-breaking-changes-detected-by-the-tool) section later in this topic.</span></span>

> [!NOTE]
> + <span data-ttu-id="91ca8-113">このトピックの一覧には、ツールが検出できる互換性に影響するすべての変更が含まれているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="91ca8-113">The list in this topic doesn't include all the breaking changes that the tool can detect.</span></span>
> + <span data-ttu-id="91ca8-114">このツールでは、互換性に影響するすべての変更を検出できるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="91ca8-114">The tool doesn't detect all breaking changes.</span></span>

## <a name="what-the-tool-doesnt-detect"></a><span data-ttu-id="91ca8-115">ツールで検出されないもの</span><span class="sxs-lookup"><span data-stu-id="91ca8-115">What the tool doesn't detect</span></span>

<span data-ttu-id="91ca8-116">このツールでは、データの比較によって識別できる、互換性に影響する変更のみが検出されます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-116">The tool detects only breaking changes that can be identified by comparing data.</span></span> <span data-ttu-id="91ca8-117">たとえば、次のような場合に発生する可能性のある、互換性に影響する変更は検出されません。</span><span class="sxs-lookup"><span data-stu-id="91ca8-117">For example, it doesn't detect the following breaking changes that often occur:</span></span>

+ <span data-ttu-id="91ca8-118">保護されたメソッドまたはパブリック メソッドへの参照が削除されます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-118">The reference to a protected or public method is removed.</span></span>
+ <span data-ttu-id="91ca8-119">メソッドの責任が変更されます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-119">The responsibility of a method is changed.</span></span>

## <a name="using-the-tool"></a><span data-ttu-id="91ca8-120">ツールの使用</span><span class="sxs-lookup"><span data-stu-id="91ca8-120">Using the tool</span></span>

<span data-ttu-id="91ca8-121">このツールを使用すると、新しいバージョンが置き換えるバージョンに対して持つメタデータの互換性の問題を検出することができます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-121">You can use the tool to detect metadata compatibility issues that a new version has against the version that it's replacing.</span></span> <span data-ttu-id="91ca8-122">Microsoft は、このツールを使用して、新たな月次更新が前回の月次更新と比較してどのような互換性に影響する変更があったかを検出します。</span><span class="sxs-lookup"><span data-stu-id="91ca8-122">Microsoft uses the tool to detect any breaking changes that a new monthly update has against the previous monthly update.</span></span>

### <a name="usage"></a><span data-ttu-id="91ca8-123">使用状況</span><span class="sxs-lookup"><span data-stu-id="91ca8-123">Usage</span></span>

```console
CompatibilityChecker.exe -BaselineDirectory=\<Path to baseline metadata\> -CurrentDirectory=\<Path to current metadata\> -ModuleName=\<Module name\> -OutputFile=\<Output file path\> -LogFile=\<Log file path\>
```

### <a name="example"></a><span data-ttu-id="91ca8-124">例</span><span class="sxs-lookup"><span data-stu-id="91ca8-124">Example</span></span>

```console
CompatibilityChecker.exe -BaselineDirectory="\\servername\archive\Build1\BaselineMetadata" -CurrentDirectory="E:\\MyCode\\retail\\amd64\\BaselineMetadata" -ModuleName="Directory"
-OutputFile="E:\\Logs\\Directory\\Diagnostics.xml" -LogFile="E:\\Logs\\Directory\\Checkerlog.txt"
```

### <a name="description"></a><span data-ttu-id="91ca8-125">説明</span><span class="sxs-lookup"><span data-stu-id="91ca8-125">Description</span></span>

<span data-ttu-id="91ca8-126">このツールは、現在のメタデータと指定されたベースラインのメタデータを比較することで、互換性に影響する変更を識別します。</span><span class="sxs-lookup"><span data-stu-id="91ca8-126">The tool identifies breaking changes by comparing the current metadata with specified baseline metadata.</span></span>

<span data-ttu-id="91ca8-127">次のパスを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-127">You must specify the following paths:</span></span>

+ <span data-ttu-id="91ca8-128">**BaselineDirectory** – ベースラインとなるメタデータのパス。</span><span class="sxs-lookup"><span data-stu-id="91ca8-128">**BaselineDirectory** – The path of the baseline metadata.</span></span>
+ <span data-ttu-id="91ca8-129">**CurrentDirectory** – 現在の (新しい) メタデータのパス。</span><span class="sxs-lookup"><span data-stu-id="91ca8-129">**CurrentDirectory** – The path of the current (new) metadata.</span></span>
+ <span data-ttu-id="91ca8-130">**OutputFile** – 互換性に影響する変更の一覧を含むファイルのパス。</span><span class="sxs-lookup"><span data-stu-id="91ca8-130">**OutputFile** – The path of the file that contains the list of breaking changes.</span></span>

<span data-ttu-id="91ca8-131">次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-131">The following rules apply:</span></span>

+ <span data-ttu-id="91ca8-132">ツールを実行する前に、現在のメタデータをコンパイルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-132">You must compile the current metadata before you run the tool.</span></span>
+ <span data-ttu-id="91ca8-133">*OutputFile* – ファイルには、ツールが識別した互換性に影響する変更のリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="91ca8-133">The *OutputFile* file contains the list of breaking changes that the tool identifies.</span></span>
+ <span data-ttu-id="91ca8-134">*BaselineDirectory* ディレクトリが存在し、指定されたモジュールとその依存関係 (モジュールに依存関係がある場合) のメタデータが必要です。</span><span class="sxs-lookup"><span data-stu-id="91ca8-134">The *BaselineDirectory* directory must exist and must have the metadata for the specified module and its dependencies (if the module has any dependencies).</span></span>
+ <span data-ttu-id="91ca8-135">*BaselineDirectory* および *currentdirectory* のメタデータパスには、 *staticmetadata* のメタデータを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-135">The metadata paths for *BaselineDirectory* and *CurrentDirectory* should have metadata for *StaticMetadata*.</span></span> <span data-ttu-id="91ca8-136">このメタデータは、指定したパスの **staticmetadata** という名前のフォルダに存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-136">This metadata should be present in a folder that is named **StaticMetadata** in the specified paths.</span></span>
+ <span data-ttu-id="91ca8-137">モデルの無視リストにエントリを追加することで、ツールが識別したすべての互換性に影響する変更を抑制することができます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-137">You can suppress any breaking change that the tool identifies by adding an entry to the model's ignore list.</span></span> <span data-ttu-id="91ca8-138">このファイルは、モデルの **AxIgnoreDiagnosticList** フォルダに存在します。</span><span class="sxs-lookup"><span data-stu-id="91ca8-138">This file is present in the **AxIgnoreDiagnosticList** folder for the model.</span></span>

## <a name="list-of-breaking-changes-detected-by-the-tool"></a><span data-ttu-id="91ca8-139">ツールが検出した互換性に影響のある変更の一覧</span><span class="sxs-lookup"><span data-stu-id="91ca8-139">List of breaking changes detected by the tool</span></span>

> [!NOTE]
> <span data-ttu-id="91ca8-140">メタデータの互換性の変更は、ツールにて互換性に影響ありとして定義されている場合にのみ、互換性に影響のある変更として識別されます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-140">The tool identifies metadata compatibility changes as breaking changes only if they have been defined as breaking in the tool.</span></span>

### <a name="class-members"></a><span data-ttu-id="91ca8-141">クラス メンバー</span><span class="sxs-lookup"><span data-stu-id="91ca8-141">Class members</span></span>

+ <span data-ttu-id="91ca8-142">**保護されたクラス メンバまたはパブリック クラス メンバのアクセス モディファイアの変更 (メンバを読み取り専用にすることも含む)** – コンシューマーは、フィールドからの読み取りや、フィールドへの値の割り当てを行っている場合があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-142">**Changing the access modifier of protected or public class members (including making a member read-only)** – Consumers might have read from the field or assigned values to it.</span></span>
+ <span data-ttu-id="91ca8-143">**パブリックまたは保護されたクラス レベルのメンバーを削除するか名前を変更する** – ユーザーは、拡張クラスでこれらのメンバーを使用している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-143">**Deleting or renaming public or protected class-level members** – Consumers might be using these members in some extension classes.</span></span>

### <a name="methods"></a><span data-ttu-id="91ca8-144">メソッド</span><span class="sxs-lookup"><span data-stu-id="91ca8-144">Methods</span></span>

+ <span data-ttu-id="91ca8-145">**保護メソッドまたはパブリック メソッド** のメソッドシグネチャを変更すると、メソッドのラッパーと呼び出し元が破損します。</span><span class="sxs-lookup"><span data-stu-id="91ca8-145">**Changing the method signature of a protected or public method** – Wrappers and callers of the method will be broken.</span></span>
+ <span data-ttu-id="91ca8-146">**保護メソッドまたはパブリック メソッドを使用しない** – コンシューマーは、メソッドをラップまたは上書きする場合があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-146">**Making a protected or public method obsolete** – Consumers might be wrapping or overriding the methods.</span></span>

### <a name="classes-and-interfaces"></a><span data-ttu-id="91ca8-147">クラスおよびインターフェイス</span><span class="sxs-lookup"><span data-stu-id="91ca8-147">Classes and interfaces</span></span>

+ <span data-ttu-id="91ca8-148">**クラスに最終化する** – ユーザーが派生タイプを作成した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-148">**Making a class final** – Consumers might have created a derived type.</span></span>
+ <span data-ttu-id="91ca8-149">**クラスの抽象化** – コンシューマーがクラスのインスタンスを作成している場合があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-149">**Making a class abstract** – Consumers might be instantiating the class.</span></span>
+ <span data-ttu-id="91ca8-150">**クラスに抽象メソッドを追加する**: ユーザーは、派生タイプを作成した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-150">**Adding an abstract method to a class** – Consumers might have created a derived type.</span></span>
+ <span data-ttu-id="91ca8-151">**メソッドをインターフェイスに追加する**: 消費者は、独自の種類でインターフェイスを実装した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-151">**Adding a method to an interface** – Consumers might have implemented the interface on their own type.</span></span>
+ <span data-ttu-id="91ca8-152">**パブリック クラスを古い形式にし、クラスのインスタンス化を停止する**: ユーザーは、インスタンス メソッドをオーバーライド、折り返し、またはサブスクライブしている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-152">**Making a public class obsolete and stopping instantiation of the class** – Consumers might have overridden, wrapped, or subscribed to the instance methods.</span></span>

### <a name="delegates"></a><span data-ttu-id="91ca8-153">委任</span><span class="sxs-lookup"><span data-stu-id="91ca8-153">Delegates</span></span>

+ <span data-ttu-id="91ca8-154">**シグネチャにおける変更** – ユーザーは、動的に登録をしている場合があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-154">**Any change in signature** – Consumers might have subscribed dynamically.</span></span>

### <a name="tables"></a><span data-ttu-id="91ca8-155">テーブル</span><span class="sxs-lookup"><span data-stu-id="91ca8-155">Tables</span></span>

<span data-ttu-id="91ca8-156">次のいずれかの変更を行うと、テーブルの拡張子とテーブルのフィールドに対するテーブル参照が壊れることになります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-156">Any of the following changes will break table extensions and table references to tables and table fields:</span></span>

+ <span data-ttu-id="91ca8-157">テーブル フィールド、フィールド グループ、インデックス、テーブルのマッピング、テーブルの関連付けを削除または名前変更する</span><span class="sxs-lookup"><span data-stu-id="91ca8-157">Deleting or renaming table fields, field groups, indexes, table mappings, or table relations</span></span>
+ <span data-ttu-id="91ca8-158">これらテーブルのプロパティ変更: **Extends**、**suportinheritance**、**TableType**、**SaveDataPerCompany**、**SaveDataPerPartition**</span><span class="sxs-lookup"><span data-stu-id="91ca8-158">Modifying these table properties: **Extends**, **SuportInheritance**, **TableType**, **SaveDataPerCompany.Yes**, or **SaveDataPerPartition**</span></span>
+ <span data-ttu-id="91ca8-159">これらのテーブル フィールドのプロパティの変更: **ExtendedDataType**、**Scale**、**文字列サイズ**</span><span class="sxs-lookup"><span data-stu-id="91ca8-159">Modifying these table field properties: **ExtendedDataType**, **Scale**, or **String size**</span></span>
+ <span data-ttu-id="91ca8-160">次のテーブル インデックス プロパティを変更する：**AllowDuplicates.No** または **indextype**</span><span class="sxs-lookup"><span data-stu-id="91ca8-160">Modifying these table index properties: **AllowDuplicates.No** or **IndexType**</span></span>

### <a name="forms"></a><span data-ttu-id="91ca8-161">フォーム</span><span class="sxs-lookup"><span data-stu-id="91ca8-161">Forms</span></span>

<span data-ttu-id="91ca8-162">次のいずれかの変更を行うと、コントロールまたはメソッドを参照するフォームの拡張機能が解除されます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-162">Any of the following changes will break form extensions that reference the controls or methods:</span></span>

+ <span data-ttu-id="91ca8-163">フォーム コントロール、フォーム データソース、フォーム データソース フィールドの削除または名前の変更。</span><span class="sxs-lookup"><span data-stu-id="91ca8-163">Deleting or renaming form controls, form data sources, and form data source fields.</span></span>
+ <span data-ttu-id="91ca8-164">メソッドに対して中断するすべての変更は、フォーム メソッドについても中断されます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-164">All changes that are breaking for methods are also breaking for form methods.</span></span>

### <a name="enumerations-enums"></a><span data-ttu-id="91ca8-165">列挙 (列挙)</span><span class="sxs-lookup"><span data-stu-id="91ca8-165">Enumerations (enums)</span></span>

+ <span data-ttu-id="91ca8-166">次のプロパティの変更：**IsExtensible** または **Value**</span><span class="sxs-lookup"><span data-stu-id="91ca8-166">Modifying these properties: **IsExtensible** or **Value**</span></span>

### <a name="extended-data-types-edts"></a><span data-ttu-id="91ca8-167">拡張データ型 (EDTs)</span><span class="sxs-lookup"><span data-stu-id="91ca8-167">Extended data types (EDTs)</span></span>

+ <span data-ttu-id="91ca8-168">これらプロパティの変更：**Extends**、**EnumType**、**Scale**</span><span class="sxs-lookup"><span data-stu-id="91ca8-168">Modifying these properties: **Extends**, **EnumType**, or **Scale**</span></span>

### <a name="entities"></a><span data-ttu-id="91ca8-169">エンティティ</span><span class="sxs-lookup"><span data-stu-id="91ca8-169">Entities</span></span>

+ <span data-ttu-id="91ca8-170">テーブルに対して中断するすべての変更は、エンティティについても中断されます。</span><span class="sxs-lookup"><span data-stu-id="91ca8-170">All changes that are breaking for tables are also breaking for entities.</span></span>
+ <span data-ttu-id="91ca8-171">パブリック エンティティの名前変更。</span><span class="sxs-lookup"><span data-stu-id="91ca8-171">Renaming a public entity.</span></span>

### <a name="labels"></a><span data-ttu-id="91ca8-172">ラベル (複数)</span><span class="sxs-lookup"><span data-stu-id="91ca8-172">Labels</span></span>

+ <span data-ttu-id="91ca8-173">**ラベルの変更または削除** – ユーザーがラベル テキストと渡されたパラメータの現在のコンテキストでラベルを使用している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-173">**Modifying or deleting a label** – Consumers might be using the label in the current context of the label text and the parameters that were passed.</span></span> <span data-ttu-id="91ca8-174">既存のラベルを変更するのではなく、新しいラベルを追加することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="91ca8-174">We recommend that you add new labels instead of changing existing labels.</span></span>

### <a name="application-elements"></a><span data-ttu-id="91ca8-175">申請の要素</span><span class="sxs-lookup"><span data-stu-id="91ca8-175">Application elements</span></span>

+ <span data-ttu-id="91ca8-176">**要素を削除する** – ユーザーは、要素の存在にコンパイル時の依存関係を持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="91ca8-176">**Removing any element** – Consumers might have a compile-time dependency on the existence of the element.</span></span>
