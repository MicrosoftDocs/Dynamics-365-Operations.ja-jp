---
title: "侵入的なカスタマイズ"
description: "このトピックは、侵襲性のあるカスタマイズの特性を定義します。"
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: 
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d75a0dace6a2c7b214d70ebe77cef1ab858fb542
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="intrusive-customizations"></a><span data-ttu-id="477ba-103">侵入的なカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="477ba-103">Intrusive customizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="477ba-104">このトピックは、侵襲性のあるカスタマイズの特性を定義します。</span><span class="sxs-lookup"><span data-stu-id="477ba-104">This topic defines the characteristics of an intrusive customization.</span></span> <span data-ttu-id="477ba-105">侵入的なカスタマイズは、継続的なアップグレードの費用をゼロに維持する主要な障害です。</span><span class="sxs-lookup"><span data-stu-id="477ba-105">Intrusive customizations are the major obstacle to keeping continuous upgrade costs close to zero.</span></span> <span data-ttu-id="477ba-106">面倒なカスタマイズには、ツールによってなくすことができる種類もありますが、それ以外の種類は引き続き作成者が拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-106">Some types of intrusive customizations can be prevented by tooling, whereas other types remain the responsibility of the author of the extension.</span></span> <span data-ttu-id="477ba-107">X++ コンパイラと Microsoft Visual Studio デザイナーでは、いくつかの種類の侵入的なカスタマイズが禁止されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-107">The X++ compiler and Microsoft Visual Studio designers will prevent some types of intrusive customizations.</span></span> <span data-ttu-id="477ba-108">ただし、侵入的なカスタマイズのサブセットはツールよって検出できませんが、継続的なアップグレードを実行しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-108">However, a subset of intrusive customizations can't be detected by tooling but might still prevent continuous upgrades.</span></span> <span data-ttu-id="477ba-109">最終的には、開発者は不注意なカスタマイズを避ける責任があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-109">Ultimately, the developer is responsible for avoiding intrusive customizations.</span></span>

<span data-ttu-id="477ba-110">次のいずれかの原則に違反しているカスタマイズは侵入的です。</span><span class="sxs-lookup"><span data-stu-id="477ba-110">A customization that violates any of the following principles is intrusive.</span></span>

## <a name="dont-change-type-definitions"></a><span data-ttu-id="477ba-111">タイプの定義を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-111">Don't change type definitions</span></span>
<span data-ttu-id="477ba-112">タイプはその定義によって参照されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-112">Types are referenced by their definition.</span></span> <span data-ttu-id="477ba-113">タイプの定義の変更は大きな変更であり、すべての参照を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-113">A change to a type’s definition is a breaking change and requires that all references be updated.</span></span> <span data-ttu-id="477ba-114">(たとえば、タイプをホストするモデルで) 今後の参照が正しく実装されるよう確認することが重要です。</span><span class="sxs-lookup"><span data-stu-id="477ba-114">It's impossible to ensure that future references will be implemented correctly (for example, in the model that hosts the type).</span></span> <span data-ttu-id="477ba-115">これにはいくつかの意味があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-115">There are several implications:</span></span>

+ <span data-ttu-id="477ba-116">メソッド シグネチャを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-116">Don't change a method signature.</span></span> <span data-ttu-id="477ba-117">メソッド シグネチャには、戻り値の型、名前 (大文字と小文字の区別を含む)、およびパラメーター (オプションのパラメーターを含む) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="477ba-117">The method signature includes the return type, the name (which includes casing), and the parameters (which include optional parameters).</span></span>
+ <span data-ttu-id="477ba-118">インターフェイスおよびテーブル マップの実装者の要件を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-118">Don't change requirements for implementers of interfaces and table maps.</span></span> <span data-ttu-id="477ba-119">たとえば、新しいメソッドをインターフェイスに、または新しいフィールドをテーブル マップに追加しないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-119">For example, don't add a new method to an interface or a new field to a table map.</span></span>
+ <span data-ttu-id="477ba-120">抽象クラスから派生したクラスの要件を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-120">Don't change requirements for classes that are derived from abstract classes.</span></span> <span data-ttu-id="477ba-121">たとえば、クラスに新しい抽象メソッドを追加しないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-121">For example, don't add a new abstract method to a class.</span></span>
+ <span data-ttu-id="477ba-122">タイプまたはメンバーのアクセス修飾子を減らさないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-122">Don't reduce access modifiers for types or members.</span></span> <span data-ttu-id="477ba-123">たとえば、クラス、テーブル、またはメソッドをパブリックからプライベートに変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-123">For example, don't change classes, tables, or methods from public to private.</span></span>
+ <span data-ttu-id="477ba-124">テーブルまたはデータ エンティティで定義されている制約を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-124">Don't change constraints that are defined on a table or a data entity.</span></span> <span data-ttu-id="477ba-125">制約には、編集、必須の制約、一意性の制約、および参照の制約を許可することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="477ba-125">Constraints include allowing editing, mandatory constraints, uniqueness constraints, and referential constraints.</span></span>

## <a name="dont-break-encapsulation"></a><span data-ttu-id="477ba-126">カプセル化を中止しない</span><span class="sxs-lookup"><span data-stu-id="477ba-126">Don't break encapsulation</span></span>
<span data-ttu-id="477ba-127">モデルの作成者は、カプセル化されたコードとタイプを管理し続けて製品を改良することができる必要があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-127">The author of a model must be able improve the product by remaining in control of encapsulated code and types.</span></span> <span data-ttu-id="477ba-128">モデルの所有者は、事前に通知せず、拡張機能およびカスタマイズの下位に影響を及ぼすことなく、自由にカプセル化されたコードを変更および削除できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-128">Model owners must be able to change and delete encapsulated code and types at will, without prior notice, and without risk of downstream impact on extensions and customizations.</span></span> <span data-ttu-id="477ba-129">たとえば、プライベート メソッドを削除された場合、カプセル化は中断されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-129">Encapsulation is broken if, for example, a private method is deleted.</span></span> <span data-ttu-id="477ba-130">次に、いくつか関連事項を示します。</span><span class="sxs-lookup"><span data-stu-id="477ba-130">Here are some of the implications:</span></span>

+ <span data-ttu-id="477ba-131">タイプまたはメンバーのアクセス修飾子を増やさないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-131">Don't increase access modifiers for types or members.</span></span> <span data-ttu-id="477ba-132">たとえば、クラス、テーブル、またはメソッドをプライベートからパブリックに変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-132">For example, don't change classes, tables, or methods from private to public.</span></span>
+ <span data-ttu-id="477ba-133">変更のために何かを閉じる必要がある場合は、カスタマイズ動作のためににそれを開けることはできません。</span><span class="sxs-lookup"><span data-stu-id="477ba-133">If something should be closed for modification, don't open it for customizing behavior.</span></span> <span data-ttu-id="477ba-134">拡張子の機能は、拡張性に向けオープンであるように設計されなければならないが、変更のためクローズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-134">Extension capabilities must be designed as open for extensibility but closed for modification.</span></span>
            
## <a name="be-additive-in-nature"></a><span data-ttu-id="477ba-135">本質的に付加</span><span class="sxs-lookup"><span data-stu-id="477ba-135">Be additive in nature</span></span>
<span data-ttu-id="477ba-136">拡張機能の一部として追加された機能を通じて新しい動作が有効になります。</span><span class="sxs-lookup"><span data-stu-id="477ba-136">New behaviors are enabled through added functionality as part of extensions.</span></span> <span data-ttu-id="477ba-137">拡張子の機能は、拡張子機能で設計および拡張子用にオープンされていなければならず、同じインストールで並行して存在する複数の拡張子をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-137">Extension capabilities must be designed in and open for extensions, and they must support multiple extensions that exist side by side in the same installation.</span></span> <span data-ttu-id="477ba-138">これにはいくつかの意味があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-138">There are several implications:</span></span>

+ <span data-ttu-id="477ba-139">オーバーレイしないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-139">Don't overlayer.</span></span> <span data-ttu-id="477ba-140">オーバーレイヤーは、既定の実装を置き換え、複数のソリューションが同じ要素を変更できないようにします。</span><span class="sxs-lookup"><span data-stu-id="477ba-140">Overlayering replaces the default implementation and prevents multiple solutions from changing the same element.</span></span>
+ <span data-ttu-id="477ba-141">標準的な機能の特性を大幅に変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-141">Don't significantly change the characteristics of the standard functionality.</span></span> <span data-ttu-id="477ba-142">これらの特性には、ユーザー エクスペリエンスとパフォーマンスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="477ba-142">These characteristics include the user experience and performance.</span></span> <span data-ttu-id="477ba-143">たとえば、拡張子がインストールされているが使用されていない場合、パフォーマンスが低下することはありません。</span><span class="sxs-lookup"><span data-stu-id="477ba-143">For example, performance must not be adversely affected if an extension is installed but isn't used.</span></span>
+ <span data-ttu-id="477ba-144">**EventHandlerResult** クラスで結果を無条件に設定しないでください。**XppPrePostArgs** クラスで戻り値を無条件に設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-144">Don't unconditionally set results in **EventHandlerResult** classes, and don't unconditionally set return values in **XppPrePostArgs** classes.</span></span>
+ <span data-ttu-id="477ba-145">置換ロジックがリスコフの置換原則に準拠していない限り、既定では、既存の動作を置き換えないでください。</span><span class="sxs-lookup"><span data-stu-id="477ba-145">Don't replace existing behavior by default, unless the replacing logic conforms to the Liskov Substitution Principle.</span></span>  

> [!NOTE]
> <span data-ttu-id="477ba-146">拡張機能の作成者は、これらの原則に違反しないようにする責任があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-146">The author of the extension is responsible for not violating these principles.</span></span>

