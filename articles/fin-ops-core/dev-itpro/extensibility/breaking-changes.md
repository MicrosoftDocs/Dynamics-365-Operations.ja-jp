---
title: 変更の分割
description: このトピックでは、分割変更について説明します。
author: smithanataraj
manager: AnnBe
ms.date: 09/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 76936d14ae094133a91058e6089df4a0695ceb01
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987254"
---
# <a name="breaking-changes"></a><span data-ttu-id="ec13e-103">変更の分割</span><span class="sxs-lookup"><span data-stu-id="ec13e-103">Breaking changes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec13e-104">ソリューションを拡張可能にすると、後で拡張ポイントを壊さずに済むことにもなります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-104">When you make your solution extensible, you also help guarantee that you won't break the extension points later.</span></span> <span data-ttu-id="ec13e-105">分割変更は、コードのユーザーを分割できる任意の変更です。</span><span class="sxs-lookup"><span data-stu-id="ec13e-105">A breaking change is any change that can break a consumer of your code.</span></span>

<span data-ttu-id="ec13e-106">このトピックでは、コードを分割できる変更のタイプを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="ec13e-106">This topic lists some of the types of changes that can break your code.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="ec13e-107">このリストは、包括的ではありません。</span><span class="sxs-lookup"><span data-stu-id="ec13e-107">This list isn't exhaustive.</span></span> <span data-ttu-id="ec13e-108">ここに登録されていない他のタイプの変更が分割変更となることもあります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-108">Other types of changes that aren't listed here could also be breaking changes.</span></span>

## <a name="data-model-changes"></a><span data-ttu-id="ec13e-109">データ モデルの変更</span><span class="sxs-lookup"><span data-stu-id="ec13e-109">Data model changes</span></span>

### <a name="general"></a><span data-ttu-id="ec13e-110">一般</span><span class="sxs-lookup"><span data-stu-id="ec13e-110">General</span></span>
<span data-ttu-id="ec13e-111">データ モデルの変更で、データ アップグレード スクリプトを実行する必要がある場合は、ユーザーがデータ モデルを同期できなくなったり、データにアクセスできなくなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-111">If any data model change requires that a data upgrade script be run, consumers might no longer be able to synchronize their data model, or they might lose access to data.</span></span>

### <a name="data-types"></a><span data-ttu-id="ec13e-112">データ型</span><span class="sxs-lookup"><span data-stu-id="ec13e-112">Data types</span></span>
+ <span data-ttu-id="ec13e-113">**列挙を拡張可能から拡張不可に変更する**: ユーザーは、列挙の拡張を持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-113">**Changing an enumeration (enum) from extensible to non-extensible** – Consumers might have extensions to the enum.</span></span>
+ <span data-ttu-id="ec13e-114">**列挙を拡張不可から拡張可能に変更する**: ユーザーは、比較で列挙を使用している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-114">**Changing an enum from non-extensible to extensible** – Consumers might be using the enums in comparisons.</span></span> <span data-ttu-id="ec13e-115">詳細については、[拡張可能な列挙の記述](extensible-enums.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec13e-115">For more details, see [Write extensible enums](extensible-enums.md).</span></span>
+ <span data-ttu-id="ec13e-116">**実数型の拡張データ型 (EDT) の小数点以下の精度を下げる**: ユーザーは、精度を使用するデータを入力する機能に依存関係を持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-116">**Decreasing the decimal precision of an extended data type (EDT) of the real type** – Consumers might have dependencies on the ability to enter data that uses the precision.</span></span>
+ <span data-ttu-id="ec13e-117">**文字列型の EDT のサイズを小さく**: ユーザーは文字列のサイズに依存関係を持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-117">**Decreasing the size of an EDT of the string type** – Consumers might have dependencies on the size of the string.</span></span>
+ <span data-ttu-id="ec13e-118">**別の EDT を拡張することにより EDT を特殊化する**: ユーザーは、文字列の長さ、または EDT への小数点以下の精度の拡張を持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-118">**Specializing the EDT by making it extend another EDT** – Consumers might have string length or decimal precision extensions to the EDT.</span></span>
+ <span data-ttu-id="ec13e-119">**列挙が拡張可能な場合に、列挙型の EDT の列挙型を変更する**: ユーザーは、列挙の拡張を持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-119">**Changing the enum type of an EDT of the enum type when the enum is extensible** – Consumers might have extensions to the enum.</span></span>
 
### <a name="data-model"></a><span data-ttu-id="ec13e-120">データ モデル</span><span class="sxs-lookup"><span data-stu-id="ec13e-120">Data model</span></span>
+ <span data-ttu-id="ec13e-121">**テーブルを古い形式にし、情報がテーブルで入力されないようにする**: ユーザーは、情報が入力されるテーブルで依存関係を持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-121">**Making a table obsolete and stopping information from being entered in the table** – Consumers might have a dependency on the table that information is entered in.</span></span>
+ <span data-ttu-id="ec13e-122">**フィールドを古い形式にし、情報がフィールドで入力されないようにする**: ユーザーは、情報が入力されるフィールドで依存関係を持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-122">**Making a table field obsolete and stopping information from being entered in the field** – Consumers might have a dependency on the field that information is entered in.</span></span>
+ <span data-ttu-id="ec13e-123">**フィールド グループの名前を変更する**: ユーザーは、フィールド グループへの拡張、またはコードまたはメタデータの依存関係を持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-123">**Renaming a field group** – Consumers might have extensions to field group, or code or metadata dependencies to it.</span></span>
+ <span data-ttu-id="ec13e-124">**制約またはインデックスの変更**</span><span class="sxs-lookup"><span data-stu-id="ec13e-124">**Changing constraints or indexes**</span></span>
+ <span data-ttu-id="ec13e-125">**テーブル マップを古い形式にし、テーブル マップが使用されないようにする**</span><span class="sxs-lookup"><span data-stu-id="ec13e-125">**Making a table map obsolete and stopping the table map from being used**</span></span>
+ <span data-ttu-id="ec13e-126">**テーブル マップ フィールドを古い形式にする**</span><span class="sxs-lookup"><span data-stu-id="ec13e-126">**Make a table map field obsolete**</span></span>
+ <span data-ttu-id="ec13e-127">**テーブル マップ フィールドを追加する**</span><span class="sxs-lookup"><span data-stu-id="ec13e-127">**Adding a table map field**</span></span>
+ <span data-ttu-id="ec13e-128">**テーブル マップ フィールド マッピングを削除する**</span><span class="sxs-lookup"><span data-stu-id="ec13e-128">**Removing a table map field mapping**</span></span>
+ <span data-ttu-id="ec13e-129">**データ エンティティを古い形式にする**</span><span class="sxs-lookup"><span data-stu-id="ec13e-129">**Making a data entity obsolete**</span></span>
+ <span data-ttu-id="ec13e-130">**データ エンティティ フィールドを古い形式にする**</span><span class="sxs-lookup"><span data-stu-id="ec13e-130">**Making a data entity field obsolete**</span></span>

## <a name="code-changes"></a><span data-ttu-id="ec13e-131">コードの変更</span><span class="sxs-lookup"><span data-stu-id="ec13e-131">Code changes</span></span>

### <a name="class-members"></a><span data-ttu-id="ec13e-132">クラス メンバー</span><span class="sxs-lookup"><span data-stu-id="ec13e-132">Class members</span></span>
+ <span data-ttu-id="ec13e-133">**パブリックまたは保護されたクラス レベルのメンバーを削除するか名前を変更する**: ユーザーは、拡張クラスでこれらのメンバーを使用している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-133">**Deleting or renaming public or protected class-level members** – Consumers might be using these members in the extension classes.</span></span>
+ <span data-ttu-id="ec13e-134">**クラス メンバーをパブリックまたは保護から保護またはプライベートに変更する**: ユーザーは、フィールドに値をクエリ済みまたは割り当て済みの可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-134">**Changing a class member from public or protected to protected or private** – Consumers might have queried or assigned values to the field.</span></span>

### <a name="classes-and-interfaces"></a><span data-ttu-id="ec13e-135">クラスおよびインターフェイス</span><span class="sxs-lookup"><span data-stu-id="ec13e-135">Classes and interfaces</span></span>
+ <span data-ttu-id="ec13e-136">**クラスに抽象メソッドを追加する**: ユーザーは、派生タイプを作成した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-136">**Adding an abstract method to a class** – Consumers might have created a derived type.</span></span>
+ <span data-ttu-id="ec13e-137">**クラスに最終を追加する**: ユーザーは、派生タイプを作成した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-137">**Adding final to a class** – Consumers might have created a derived type.</span></span>
+ <span data-ttu-id="ec13e-138">**メソッドをインターフェイスに追加する**: 消費者は、独自の種類でインターフェイスを実装した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-138">**Adding a method to an interface** – Consumers might have implemented the interface on their own type.</span></span>
+ <span data-ttu-id="ec13e-139">**パブリック クラスを古い形式にし、クラスのインスタンス化を停止する**: ユーザーは、インスタンス メソッドをオーバーライド、折り返し、またはサブスクライブしている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-139">**Making a public class obsolete and stopping instantiation of the class** – Consumers might have overridden, wrapped, or subscribed to the instance methods.</span></span>

### <a name="methods"></a><span data-ttu-id="ec13e-140">メソッド</span><span class="sxs-lookup"><span data-stu-id="ec13e-140">Methods</span></span>
+ <span data-ttu-id="ec13e-141">**アクセス修飾子を保護またはパブリックから別のアクセス修飾子に変更する**: ユーザーは、メソッドを呼び出し、オーバーライド、折り返し、サブスクライブした可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-141">**Changing the access modifier from protected or public to another access modifier** – Consumers might have called, overridden, wrapped, or subscribed to the method.</span></span>
+ <span data-ttu-id="ec13e-142">**具体的なパブリックまたは保護されているメソッドを抽象的にする**: ユーザーは、クラスへのサブクラスを持っており、それらのサブクラスがメソッドを実装していないか、上位を呼び出す可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-142">**Making a concrete public or protected method abstract** – Consumers might have subclasses to the class, and those subclasses might not have implemented the method, or they might even call super.</span></span>
+ <span data-ttu-id="ec13e-143">**メソッド パラメーターの名前を変更する**: ユーザーは、名前によるパラメーターの依存関係を持っている可能性があります (引数または C\# から外部でなど)。</span><span class="sxs-lookup"><span data-stu-id="ec13e-143">**Renaming method parameters** – Consumers might have dependencies on parameters by name (via arguments or externally from C\#, for example).</span></span>
+ <span data-ttu-id="ec13e-144">**保護またはパブリック メソッドでメソッド パラメーターのタイプを追加、削除、または変更する**: ユーザーは、メソッドを呼び出し、オーバーライド、折り返し、サブスクライブした可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-144">**Adding, removing, or changing the type of a method parameter on a protected or public method** – Consumers might have called, overridden, wrapped, or subscribed to the method.</span></span>
+ <span data-ttu-id="ec13e-145">**保護またはパブリック メソッドで既定のメソッド パラメーターを追加または削除する**: ユーザーは、メソッドを折り返しまたはサブスクライブした可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-145">**Adding or removing a default method parameter on a protected or public method** – Consumers might have wrapped or subscribed to the method.</span></span>
+ <span data-ttu-id="ec13e-146">**メソッドの戻り値の型を変更する**: ユーザーは、メソッドを呼び出し、オーバーライド、折り返し、またはサブスクライブした可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-146">**Changing the return type of a method** – Consumers might have called, overridden, wrapped, or subscribed to the method.</span></span>
+ <span data-ttu-id="ec13e-147">**保護またはパブリック メソッドに Hookable(false) を追加する**: ユーザーは、メソッドを折り返しまたはサブスクライブした可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-147">**Adding Hookable(false) to a protected or public method** – Consumers might have wrapped or subscribed to the method.</span></span>
+ <span data-ttu-id="ec13e-148">**保護またはパブリック メソッドに Wrappable(false) を追加する**: ユーザーは、メソッドを折り返した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-148">**Adding Wrappable(false) to a protected or public method** – Consumers might have wrapped the method.</span></span>
+ <span data-ttu-id="ec13e-149">**プライベートまたは保護メソッドから Hookable(true) を削除する**: ユーザーは、メソッドをサブスクライブした可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-149">**Removing Hookable(true) from a private or protected method** – Consumers might have subscribed to the method.</span></span>
+ <span data-ttu-id="ec13e-150">**プライベートまたは保護メソッドから Wrappable(true) を削除する**: ユーザーは、メソッドを折り返した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-150">**Removing Wrappable(true) from a private method** – Consumers might have wrapped the method.</span></span>
+ <span data-ttu-id="ec13e-151">**メソッドから Replaceable(true) を削除する**: ユーザーは、条件付きでメソッドを折り返した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-151">**Removing Replaceable(true) from a method** – Consumers might have conditionally wrapped the method.</span></span>
+ <span data-ttu-id="ec13e-152">**保護またはパブリック メソッドに最終を追加する**: ユーザーは、メソッドをオーバーライド、折り返し、またはサブスクライブした可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-152">**Adding final to a protected or public method** – Consumers might have overridden, wrapped, or subscribed to the method.</span></span>
+ <span data-ttu-id="ec13e-153">**インスタンスから静的または静的からインスタンスにメソッドを変更する**: ユーザーは、メソッドを呼び出し、オーバーライド、折り返し、サブスクライブした可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-153">**Changing a method from instance to static or from static to instance** – Consumers might have called, overridden, wrapped, or subscribed to the method.</span></span>
+ <span data-ttu-id="ec13e-154">**メソッドを古い形式にし、メソッドの呼び出しを停止する**: ユーザーは、メソッドを呼び出し、オーバーライド、折り返し、またはサブスクライブしている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-154">**Making a method obsolete and stopping invocation of the method** – Consumers might have called, overridden, wrapped, or subscribed to the method.</span></span>
+ <span data-ttu-id="ec13e-155">**メソッドの責任を変更する**: ユーザーは、メソッドを呼び出し、オーバーライド、折り返し、またはサブスクライブした可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-155">**Changing the responsibility of a method** – Consumers might have called, overridden, wrapped, or subscribed to the method.</span></span>
+ <span data-ttu-id="ec13e-156">**メソッドへの参照を削除する**: ユーザーは、メソッドをオーバーライド、折り返し、またはサブスクライブしている可能性があり、ロジックが実行されることを期待している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-156">**Removing the reference to a method** – Consumers might have overridden, wrapped, or subscribed to the method, and they might expect their logic to run.</span></span>

### <a name="delegates"></a><span data-ttu-id="ec13e-157">委任</span><span class="sxs-lookup"><span data-stu-id="ec13e-157">Delegates</span></span>
+ <span data-ttu-id="ec13e-158">**シグネチャで変更を行う**: ユーザーは、動的にサブスクライブしている場合があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-158">**Making any change in signature** – Consumers might have subscribed dynamically.</span></span>
+ <span data-ttu-id="ec13e-159">**デリゲートへの参照を削除する**: ユーザーは、サブスクライブしている可能性があり、ロジックが実行されることを期待している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-159">**Removing the reference to a delegate** – Consumers might have subscribed, and they might expect their logic to run.</span></span>

## <a name="label-changes"></a><span data-ttu-id="ec13e-160">ラベルの変更</span><span class="sxs-lookup"><span data-stu-id="ec13e-160">Label changes</span></span>
+ <span data-ttu-id="ec13e-161">**ラベルを変更または削除する**: ユーザーは、ラベル テキストの現在のコンテキストにあるラベルと渡されたパラメーターなどを使用している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-161">**Modifying or deleting a label** – Consumers might be using the label in the current context of the label text and the parameters that were passed, and so on.</span></span> <span data-ttu-id="ec13e-162">今後は、ラベルの変更が発生した場合は新しいラベルを追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ec13e-162">We recommend that, going forward, you add new labels in the event of a label change.</span></span>

## <a name="application-element-changes"></a><span data-ttu-id="ec13e-163">アプリケーション要素の変更</span><span class="sxs-lookup"><span data-stu-id="ec13e-163">Application element changes</span></span>
+ <span data-ttu-id="ec13e-164">**要素を削除する**: ユーザーは、要素の存在にコンパイル時間の依存関係を持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-164">**Removing any element** – Consumers might have a compile time dependency on the existence of the element.</span></span>
     
## <a name="metadata-extensions"></a><span data-ttu-id="ec13e-165">メタデータの拡張</span><span class="sxs-lookup"><span data-stu-id="ec13e-165">Metadata extensions</span></span>
+ <span data-ttu-id="ec13e-166">**メタデータまたは拡張クラスの名前付けガイドラインに従わない**: ユーザーは、同じ名前を持つ要素を持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec13e-166">**Not following the naming guidelines for metadata or augmentation classes** – Consumers might have elements that have the same name.</span></span>
