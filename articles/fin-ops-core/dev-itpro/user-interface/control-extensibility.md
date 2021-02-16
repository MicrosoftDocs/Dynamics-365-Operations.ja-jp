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
# <a name="control-extensibility"></a>コントロールの拡張機能

[!include [banner](../includes/banner.md)]

この記事では、開発者がユーザー インターフェイスを拡張し、新しいユーザー インターフェイス パターンを定義できるようにするアーキテクチャについて説明します。

既存のアプリケーション ユーザー インターフェイス (UI) を拡張、および完全に新しい UI パターンを定義して魅力的な新しいユーザー エクスペリエンスを作成することができます。 HTML5、CSS3、jQuery などの最新ツールを使用することにより、開発者は業務データのカスタマイズされた視覚エフェクトを定義し、プログラムの相互作用パターンを大幅に強化することができます。

## <a name="server-side-architecture"></a>サーバー側アーキテクチャ

コントロール拡張フレームワークは、サーバー側データ アクセスおよびビジネス ロジックを開発するために既存の使い慣れた X++ 言語を活用します。 開発者が拡張可能なコントロールを作成するために書くコードに人為的な制限はありません。 代わりに、開発者は一連の X++ クラスおよびメソッドの属性を通じてモデリング経験およびランタイムの動作を宣言的に定義できます。 開発者は、1 つのクラスをデザイン時の動作 (X++ Build クラス) に、1 つのクラスを実行時の動作 (X++ RunTime クラス) に定義します。

- X++ ビルド クラスでは、属性によってプロパティ シートでのカスタム プロパティ、子コントロールの追加、追加のモデリング コンポーネントなどのデザイン時の動作を定義できます。
- X++ ランタイム クラスでは、拡張可能コントロールがクライアントからアクセスする実行時のプロパティとコマンドを定義するために属性が使用されます。 X++ ランタイム クラスは、プロパティ シートで指定されている値とデータ バインディングに基づき、X++ 構築クラスを使用して、実行時のプロパティを初期化します。

## <a name="client-side-architecture"></a>クライアント側のアーキテクチャ

コントロールのクライアント側の動作は、HTML と JavaScript を使用して定義されます。 モデル - ビュー - ViewModel アーキテクチャにおいては、コントロールの HTML が View で、JavaScript は ビュー モデルです。 コントロール拡張フレームワークは、HTML ビューの要素を JavaScript ビュー モデルでデータ フィールドおよびプロパティにバインドできるようにする HTML 形式のバインディング構文を提供します。 さらに、フレームワークによって、ビュー モデル プロパティや業務データの変更に対処できる条件式や論理評価を基に定義する視覚化動作が可能です。 JavaScript ビュー モデルは、コントロールの X++ ランタイムで定義されているプロパティとコマンドに基づいて、実行時に自動的に生成されます。 この自動的に生成されたビュー モデルを使用すると、開発者は X++ で定義されているプロパティとコマンドを使用する HTML ビューを定義できます。 開発者が追加のクライアント側のプロパティとコマンドを必要とする場合や、HTML ビューで宣言的に定義できない視覚化動作を実装する場合は、自動的に生成されたビュー モデルを拡張することができます。 開発者は、強力な jQuery ライブラリと組み合わせて JavaScript フレームワークを利用することができます。

## <a name="control-extensibility-architecture-overview"></a>コントロールの拡張機能アーキテクチャの概要

次の図は、関係するコンポーネントとそれらの相互関係を示しています。 [![拡張性アーキテクチャのコントロール](./media/extensibilitycontrolarchitecture.png)](./media/extensibilitycontrolarchitecture.png)
