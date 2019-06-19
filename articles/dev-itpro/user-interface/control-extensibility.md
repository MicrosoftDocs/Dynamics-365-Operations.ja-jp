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
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 27461
ms.assetid: f03f1fc6-4f8f-4f42-8e38-5ecba8eac413
ms.search.region: Global
ms.author: shshabazz
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd09487a027014423b4a0b1795deab81ca6414fd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555210"
---
# <a name="control-extensibility"></a><span data-ttu-id="0382c-103">コントロールの拡張機能</span><span class="sxs-lookup"><span data-stu-id="0382c-103">Control extensibility</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0382c-104">この記事では、開発者がユーザー インターフェイスを拡張し、新しいユーザー インターフェイス パターンを定義できるようにするアーキテクチャについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0382c-104">This article describes the architecture that lets developers extend the user interface and also define new user interface patterns.</span></span> 

<span data-ttu-id="0382c-105">既存のアプリケーション ユーザー インターフェイス (UI) を拡張、および完全に新しい UI パターンを定義して魅力的な新しいユーザー エクスペリエンスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="0382c-105">You can extend the existing application user interface (UI) and can also define entirely new UI patterns to create compelling new user experiences.</span></span> <span data-ttu-id="0382c-106">HTML5、CSS3、jQuery などの最新ツールを使用することにより、開発者は業務データのカスタマイズされた視覚エフェクトを定義し、プログラムの相互作用パターンを大幅に強化することができます。</span><span class="sxs-lookup"><span data-stu-id="0382c-106">By using modern tools such as HTML5, CSS3, and jQuery, developers can define customized visualizations of business data and drastically enhance the program's interaction patterns.</span></span>

## <a name="serverside-architecture"></a><span data-ttu-id="0382c-107">サーバー側アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="0382c-107">Serverside architecture</span></span>
<span data-ttu-id="0382c-108">コントロール拡張フレームワークは、サーバー側データ アクセスおよびビジネス ロジックを開発するために既存の使い慣れた X++ 言語を活用します。</span><span class="sxs-lookup"><span data-stu-id="0382c-108">The Control Extensibility Framework takes advantage of the existing and familiar X++ language for developing server-side data access and business logic.</span></span> <span data-ttu-id="0382c-109">開発者が拡張可能なコントロールを作成するために書くコードに人為的な制限はありません。</span><span class="sxs-lookup"><span data-stu-id="0382c-109">There are no artificial restrictions on the code that developers write to build extensible controls.</span></span> <span data-ttu-id="0382c-110">代わりに、開発者は一連の X++ クラスおよびメソッドの属性を通じてモデリング経験およびランタイムの動作を宣言的に定義できます。</span><span class="sxs-lookup"><span data-stu-id="0382c-110">Instead, developers can declaratively define the modeling experience and the run-time behavior through a set of X++ class and method attributes.</span></span> <span data-ttu-id="0382c-111">開発者は、1 つのクラスをデザイン時の動作 (X++ Build クラス) に、1 つのクラスを実行時の動作 (X++ RunTime クラス) に定義します。</span><span class="sxs-lookup"><span data-stu-id="0382c-111">A developer defines one class for the design-time behavior (the X++ Build Class) and one class for the run-time behavior (the X++ RunTime class).</span></span>

-   <span data-ttu-id="0382c-112">X++ ビルド クラスでは、属性によってプロパティ シートでのカスタム プロパティ、子コントロールの追加、追加のモデリング コンポーネントなどのデザイン時の動作を定義できます。</span><span class="sxs-lookup"><span data-stu-id="0382c-112">In the X++ Build Class, attributes enable the definition of design-time behaviors such as custom properties in the property sheet, the addition of child controls, and extra modeling components.</span></span>
-   <span data-ttu-id="0382c-113">X++ ランタイム クラスでは、拡張可能コントロールがクライアントからアクセスする実行時のプロパティとコマンドを定義するために属性が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0382c-113">In the X++ Runtime Class, attributes are used to define the run-time properties and commands that the extensible control will access from the client.</span></span> <span data-ttu-id="0382c-114">X++ ランタイム クラスは、プロパティ シートで指定されている値とデータ バインディングに基づき、X++ 構築クラスを使用して、実行時のプロパティを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0382c-114">The X++ Runtime Class consumes the X++ Build Class to initialize the run-time properties, based on the values and data bindings that are specified in the property sheet.</span></span>

## <a name="clientside-architecture"></a><span data-ttu-id="0382c-115">クライアント側のアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="0382c-115">Clientside architecture</span></span>
<span data-ttu-id="0382c-116">コントロールのクライアント側の動作は、HTML と JavaScript を使用して定義されます。</span><span class="sxs-lookup"><span data-stu-id="0382c-116">The client-side behavior for the control is defined by using HTML and JavaScript.</span></span> <span data-ttu-id="0382c-117">モデル-ビュー-ViewModel アーキテクチャにおいては、コントロールの HTML が View を構成し、JavaScript が ViewModel を構成します。</span><span class="sxs-lookup"><span data-stu-id="0382c-117">In the context of a Model-View-ViewModel architecture, the HTML for the control comprises the View, and the JavaScript comprises the ViewModel.</span></span> <span data-ttu-id="0382c-118">コントロール拡張フレームワークは、HTML ビューの要素を JavaScript ViewModel でデータ フィールドおよびプロパティにバインドできるようにする HTML 形式のバインディング構文を提供します。</span><span class="sxs-lookup"><span data-stu-id="0382c-118">The Control Extensibility Framework provides an HTML-based binding syntax that enables elements in the HTML View to be bound to data fields and properties in the JavaScript ViewModel.</span></span> <span data-ttu-id="0382c-119">さらに、フレームワークによって、ViewModel プロパティや業務データの変更に対処できる条件式や論理評価を基に定義する視覚化動作が可能です。</span><span class="sxs-lookup"><span data-stu-id="0382c-119">In addition, the framework enables visualization behavior to be defined based on conditional expressions or logical evaluations that can react to changes in ViewModel properties or business data.</span></span> <span data-ttu-id="0382c-120">JavaScript ViewModel は、コントロールの X++ ランタイムで定義されているプロパティとコマンドに基づいて、実行時に自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="0382c-120">The JavaScript ViewModel is automatically generated at run time, based on the properties and commands that are defined in the X++ runtime for the control.</span></span> <span data-ttu-id="0382c-121">この自動的に生成された ViewModel を使用すると、開発者は X++ で定義されているプロパティとコマンドを使用する HTMLビューを定義できます。</span><span class="sxs-lookup"><span data-stu-id="0382c-121">This automatically generated ViewModel lets a developer define an HTML View that consumes the properties and commands that are defined in X++.</span></span> <span data-ttu-id="0382c-122">開発者が追加のクライアント側のプロパティとコマンドを必要とする場合や、HTML ビューで宣言的に定義できない視覚化動作を実装する場合は、自動的に生成された ViewModel を拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="0382c-122">If a developer wants additional client-side properties and commands, or wants to implement visualization behavior that can't be declaratively defined in the HTML View, he or she can extend the automatically generated ViewModel.</span></span> <span data-ttu-id="0382c-123">開発者は、強力な jQuery ライブラリと組み合わせて JavaScript フレームワークを利用することができます。</span><span class="sxs-lookup"><span data-stu-id="0382c-123">The developer can take advantage of the JavaScript framework in conjunction with the powerful jQuery library.</span></span>

## <a name="control-extensibility-architecture-overview"></a><span data-ttu-id="0382c-124">コントロールの拡張機能アーキテクチャの概要</span><span class="sxs-lookup"><span data-stu-id="0382c-124">Control extensibility architecture overview</span></span>
<span data-ttu-id="0382c-125">次の図は、関係するコンポーネントとそれらの相互関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="0382c-125">The following diagram shows the artifacts that are involved and their relation to each other.</span></span> <span data-ttu-id="0382c-126">[![拡張性アーキテクチャのコントロール](./media/extensibilitycontrolarchitecture.png)](./media/extensibilitycontrolarchitecture.png)</span><span class="sxs-lookup"><span data-stu-id="0382c-126">[![Control extensibility architecture](./media/extensibilitycontrolarchitecture.png)](./media/extensibilitycontrolarchitecture.png)</span></span>





