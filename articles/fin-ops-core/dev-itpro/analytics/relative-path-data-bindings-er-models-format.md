---
title: ER モデルおよび形式のデータ バインディングにおける相対パスの使用
description: 電子申告報告ツールは、ユーザーが電子フォーマット構造を定義できるようにし、データとアルゴリズムを使用してこれらの構造を入力する方法を説明します。
author: kfend
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 54fb7d488dff1ad36e2d44b8bb9e0fa3fce7ea1b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276565"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>ER モデルおよび形式のデータ バインディングにおける相対パスの使用

[!include[banner](../includes/banner.md)]

電子申告 (ER) ツールは、ユーザーが電子フォーマット構造を定義できるようにし、アプリケーションに存在するデータとアルゴリズムを使用してこれらの構造を入力する方法を説明します。 詳細については、[電子申告 (ER) コンフィギュレーションの作成](electronic-reporting-configuration.md) を参照してください。 財務と運用のデータを取得し、それを使用して電子ドキュメントを生成するためのデータ フローを指定するには、以下を実行する必要があります。

- 設計されたドメイン固有のデータ モデルの要素に対するコンフィギュレーションされたデータ ソースをバインドします。 モデル構造と選択されたデータ ソースは、複雑な階層構造の一部であることがあります。 このため、最終バインディングは非常に大きくなり、異なるタイプのさまざまな要素 (たとえば、関係、テーブル、およびメソッド) を含むことがあります。 バインディングは読み取れず、特に所有者でない場合、確認や把握が非常に複雑になることがあります。 
- データ モデル要素と形式コンポーネントをバインドして、データ モデルから生成された形式の出力に設定するデータを定義します。

ER マッピング デザイナーの使用可能性を改善する目的でに、[相対パス](er-formula-language.md#relative-path)機能がリリースされました。 既定では、ER デザイン エクスペリエンスが有効になっているアプリケーションのすべての新しいインスタンスに対して、相対パスの表示オプションが有効になっています (Microsoft Dynamics 365 Finance、Microsoft Regulatory Configuration Service)。 この ER バインディングのプレゼンテーションと共に動作している時に、フル パスを使用しつづけられるように、相対パス パラメータを実装しています。

[![ユーザー パラメーター。](./media/relative-path-01.png)](./media/relative-path-01.png)

 
相対パス使用パラメーターが有効になっている場合、1 つの文字 @ は現在のモデル要素のバインドの親項目へのパスに置き換えられます。 バインド パス全体が短くなり、マッピング全体がより明確で、理解しやすくなります。 ほとんどの場合、データ モデルのすべてのバインドを表示するために ER デザイナーにおいて追加でスクロールする必要はありません。

[![モデル マッピング デザイナー。](./media/relative-path-02.png)](./media/relative-path-02.png)
 
新しい ER 式のデザインを開始する場合、文字を 1 つ入力するだけで親項目のフィールドへのバインドを定義することができます。

[![フォーミュラ デザイナー。](./media/relative-path-03.png)](./media/relative-path-03.png)
 
絶対パスを使用して親モデル項目のデータ ソースを変更する場合、入れ子になったすべての項目と共に、このモデル項目を新しいデータ ソースに手動で再バインドする必要があります。 相対パスの使用が有効になっていて、親項目にバインドされる新しいデータ ソースを選択した場合、この親項目に入れ子になっているすべての要素をワン クリックで自動的に再バインドできるオプションが提供されます。

[![既存のパス メッセージの置換。](./media/relative-path-04.png)](./media/relative-path-04.png)
 
入れ子になった項目の再バインドを確定すると、既存の親項目も含め、入れ子になった各項目のパスに新しい親項目が配置されます。
この機能は ER フレームワークの下位互換性を損なうことはありません。 以前に設計されたすべての ER コンフィギュレーションは、この新しい機能と共に動作し、アップグレードや変換は必要ありません。

> [!NOTE]
> モデル マッピングで入れ子になっている要素のバインディングを大量に変更することによって生じるすべての変更は、コンフィギュレーションの差分 (変更の追跡) に正しく保存されます。 これにより、顧客はモデル マッピングの派生バージョンを、この新しい機能を使用して変更された新しいベース バージョンに再ベースすることができます。

## <a name="additional-resources"></a>追加リソース

[ER 式の言語](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

