---
title: コントロールの拡張機能
description: この記事では、開発者がユーザー インターフェイスを拡張し、新しいユーザー インターフェイス パターンを定義できるようにするアーキテクチャについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 27461
ms.assetid: f03f1fc6-4f8f-4f42-8e38-5ecba8eac413
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0f6ef364f49fc06f9825f8c2794bc0771cc4837
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682461"
---
# <a name="control-extensibility"></a><span data-ttu-id="578b1-103">コントロールの拡張機能</span><span class="sxs-lookup"><span data-stu-id="578b1-103">Control extensibility</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="578b1-104">この記事では、開発者がユーザー インターフェイスを拡張し、新しいユーザー インターフェイス パターンを定義できるようにするアーキテクチャについて説明します。</span><span class="sxs-lookup"><span data-stu-id="578b1-104">This article describes the architecture that lets developers extend the user interface and also define new user interface patterns.</span></span>

<span data-ttu-id="578b1-105">既存のアプリケーション ユーザー インターフェイス (UI) を拡張、および完全に新しい UI パターンを定義して魅力的な新しいユーザー エクスペリエンスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="578b1-105">You can extend the existing application user interface (UI) and can also define entirely new UI patterns to create compelling new user experiences.</span></span> <span data-ttu-id="578b1-106">HTML5、CSS3、jQuery などの最新ツールを使用することにより、開発者は業務データのカスタマイズされた視覚エフェクトを定義し、プログラムの相互作用パターンを大幅に強化することができます。</span><span class="sxs-lookup"><span data-stu-id="578b1-106">By using modern tools such as HTML5, CSS3, and jQuery, developers can define customized visualizations of business data and drastically enhance the program's interaction patterns.</span></span>

## <a name="server-side-architecture"></a><span data-ttu-id="578b1-107">サーバー側アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="578b1-107">Server-side architecture</span></span>

<span data-ttu-id="578b1-108">コントロール拡張フレームワークは、サーバー側データ アクセスおよびビジネス ロジックを開発するために既存の使い慣れた X++ 言語を活用します。</span><span class="sxs-lookup"><span data-stu-id="578b1-108">The Control Extensibility Framework takes advantage of the existing and familiar X++ language for developing server-side data access and business logic.</span></span> <span data-ttu-id="578b1-109">開発者が拡張可能なコントロールを作成するために書くコードに人為的な制限はありません。</span><span class="sxs-lookup"><span data-stu-id="578b1-109">There are no artificial restrictions on the code that developers write to build extensible controls.</span></span> <span data-ttu-id="578b1-110">代わりに、開発者は一連の X++ クラスおよびメソッドの属性を通じてモデリング経験およびランタイムの動作を宣言的に定義できます。</span><span class="sxs-lookup"><span data-stu-id="578b1-110">Instead, developers can declaratively define the modeling experience and the run-time behavior through a set of X++ class and method attributes.</span></span> <span data-ttu-id="578b1-111">開発者は、1 つのクラスをデザイン時の動作 (X++ Build クラス) に、1 つのクラスを実行時の動作 (X++ RunTime クラス) に定義します。</span><span class="sxs-lookup"><span data-stu-id="578b1-111">A developer defines one class for the design-time behavior (the X++ Build Class) and one class for the run-time behavior (the X++ RunTime class).</span></span>

- <span data-ttu-id="578b1-112">X++ ビルド クラスでは、属性によってプロパティ シートでのカスタム プロパティ、子コントロールの追加、追加のモデリング コンポーネントなどのデザイン時の動作を定義できます。</span><span class="sxs-lookup"><span data-stu-id="578b1-112">In the X++ Build Class, attributes enable the definition of design-time behaviors such as custom properties in the property sheet, the addition of child controls, and extra modeling components.</span></span>
- <span data-ttu-id="578b1-113">X++ ランタイム クラスでは、拡張可能コントロールがクライアントからアクセスする実行時のプロパティとコマンドを定義するために属性が使用されます。</span><span class="sxs-lookup"><span data-stu-id="578b1-113">In the X++ Runtime Class, attributes are used to define the run-time properties and commands that the extensible control will access from the client.</span></span> <span data-ttu-id="578b1-114">X++ ランタイム クラスは、プロパティ シートで指定されている値とデータ バインディングに基づき、X++ 構築クラスを使用して、実行時のプロパティを初期化します。</span><span class="sxs-lookup"><span data-stu-id="578b1-114">The X++ Runtime Class consumes the X++ Build Class to initialize the run-time properties, based on the values and data bindings that are specified in the property sheet.</span></span>

## <a name="client-side-architecture"></a><span data-ttu-id="578b1-115">クライアント側のアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="578b1-115">Client-side architecture</span></span>

<span data-ttu-id="578b1-116">コントロールのクライアント側の動作は、HTML と JavaScript を使用して定義されます。</span><span class="sxs-lookup"><span data-stu-id="578b1-116">The client-side behavior for the control is defined by using HTML and JavaScript.</span></span> <span data-ttu-id="578b1-117">モデル - ビュー - ViewModel アーキテクチャにおいては、コントロールの HTML が View で、JavaScript は ビュー モデルです。</span><span class="sxs-lookup"><span data-stu-id="578b1-117">In the context of a Model-View-ViewModel architecture, the HTML for the control is the View, and the JavaScript is the viewmodel.</span></span> <span data-ttu-id="578b1-118">コントロール拡張フレームワークは、HTML ビューの要素を JavaScript ビュー モデルでデータ フィールドおよびプロパティにバインドできるようにする HTML 形式のバインディング構文を提供します。</span><span class="sxs-lookup"><span data-stu-id="578b1-118">The Control Extensibility Framework provides an HTML-based binding syntax that enables elements in the HTML View to be bound to data fields and properties in the JavaScript viewmodel.</span></span> <span data-ttu-id="578b1-119">さらに、フレームワークによって、ビュー モデル プロパティや業務データの変更に対処できる条件式や論理評価を基に定義する視覚化動作が可能です。</span><span class="sxs-lookup"><span data-stu-id="578b1-119">In addition, the framework enables visualization behavior to be defined based on conditional expressions or logical evaluations that can react to changes in viewmodel properties or business data.</span></span> <span data-ttu-id="578b1-120">JavaScript ビュー モデルは、コントロールの X++ ランタイムで定義されているプロパティとコマンドに基づいて、実行時に自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="578b1-120">The JavaScript viewmodel is automatically generated at run time, based on the properties and commands that are defined in the X++ runtime for the control.</span></span> <span data-ttu-id="578b1-121">この自動的に生成されたビュー モデルを使用すると、開発者は X++ で定義されているプロパティとコマンドを使用する HTML ビューを定義できます。</span><span class="sxs-lookup"><span data-stu-id="578b1-121">This automatically generated viewmodel lets a developer define an HTML View that consumes the properties and commands that are defined in X++.</span></span> <span data-ttu-id="578b1-122">開発者が追加のクライアント側のプロパティとコマンドを必要とする場合や、HTML ビューで宣言的に定義できない視覚化動作を実装する場合は、自動的に生成されたビュー モデルを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="578b1-122">If a developer wants additional client-side properties and commands, or wants to implement visualization behavior that can't be declaratively defined in the HTML View, the developer can extend the automatically generated viewmodel.</span></span> <span data-ttu-id="578b1-123">開発者は、強力な jQuery ライブラリと組み合わせて JavaScript フレームワークを利用することができます。</span><span class="sxs-lookup"><span data-stu-id="578b1-123">The developer can take advantage of the JavaScript framework in conjunction with the powerful jQuery library.</span></span>

## <a name="control-extensibility-architecture-overview"></a><span data-ttu-id="578b1-124">コントロールの拡張機能アーキテクチャの概要</span><span class="sxs-lookup"><span data-stu-id="578b1-124">Control extensibility architecture overview</span></span>

<span data-ttu-id="578b1-125">次の図は、関係するコンポーネントとそれらの相互関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="578b1-125">The following diagram shows the artifacts that are involved and their relation to each other.</span></span> <span data-ttu-id="578b1-126">[![拡張性アーキテクチャのコントロール](./media/extensibilitycontrolarchitecture.png)](./media/extensibilitycontrolarchitecture.png)</span><span class="sxs-lookup"><span data-stu-id="578b1-126">[![Control extensibility architecture](./media/extensibilitycontrolarchitecture.png)](./media/extensibilitycontrolarchitecture.png)</span></span>
