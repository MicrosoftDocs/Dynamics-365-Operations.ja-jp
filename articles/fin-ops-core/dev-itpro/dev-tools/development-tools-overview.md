---
title: Visual Studio の開発ツール
description: Visual Studio は、開発用の単一統合開発環境 (IDE) です。
author: gianugo
ms.date: 05/24/2017
ms.topic: overview
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: gianura
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 23401,  ""intro-internal
ms.assetid: ''
ms.openlocfilehash: 79e263c9cd76437116f06ae007f56ff037ded1c7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271163"
---
# <a name="development-tools-in-visual-studio"></a>Visual Studio の開発ツール

[!include [banner](../includes/banner.md)]

## <a name="what-are-the-development-tools"></a>開発ツールとは
アプリケーションの開発は、Visual Studio で行なわれます。 開発ツールは、デバッグおよびローカル テストのシナリオを含むすべての開発タスクをサポートします。 Visual Studio は、開発用の単一統合開発環境 (IDE) です。 すべてのアプリケーション開発作業がそのアプリケーションで実行されます。 このセクションでは、開発ツールのインストール時に Visual Studio に追加される主な機能の概要を説明します。

Visual Studio 2019 は、財務と運用アプリ バージョン 10.0.21 のプラットフォーム更新プログラムからサポートされます。

### <a name="application-explorer"></a>アプリケーション エクスプローラー
Visual Studio で、モデル ストアはアプリケーション エクスプローラーで表されます。 **表示** メニューで、**アプリケーション** **エクスプローラー** をクリックして開きます。 アプリケーション エクスプローラーを使用して、アプリケーションを定義するモデル ストア内の要素を参照および操作します。 次の図は、アプリケーション エクスプローラーを示しています。 詳細については、[アプリケーション エクスプローラー](application-explorer.md)を参照してください。

![アプリケーション エクスプローラー。](media/1_devotoolsconcept.png)

### <a name="the-project-template"></a>プロジェクト テンプレート
単純なアプリケーションであっても、そのモデルには多数の要素を含めることができます。 モデルに使用する要素を整理および管理するために、**業務プロジェクト** テンプレートが Visual Studio に追加されました。 このプロジェクトを使用して、モデル要素の設計、作成、およびをテストをします。 1 つの Visual Studio ソリューション内に複数のプロジェクトがあることが一般的です。 次の図は、Visual Studio ソリューションの 3 つのプロジェクトを示しています。 詳細については、[Visual Studio の財務と運用プロジェクト タイプ](projects.md) を参照してください。

![ソリューション エクスプローラー。](media/2_devotoolsconcept.png)

### <a name="element-designers"></a>要素デザイナー
Visual Studio ツールには、アプリケーション内要素の種類ごとのデザイナーが含まれています。 要素を作成または変更するときは、これらのデザイナーを使用します。 次の図は、フォーム要素の要素デザイナーを示しています。 詳細については、[要素デザイナー](element-designers.md)を参照してください。

![要素デザイナー。](media/3_devotoolsconcept.png)

### <a name="code-editor"></a>コード エディター
X++ コードは、Visual Studio 用のコード エディターに書き込まれます。 開発者がコード エディターに期待する標準機能がサポートされています。 たとえば、コードのセクションは折りたたみ可能です。 IntelliSense は、コードを書き込みまたは変更するガイダンスを提供します。 詳細については、[コード エディター機能](code-editor.md)を参照してください。

![コード エディター。](media/4_devotoolsconcept.png)

### <a name="dynamics-365-menu"></a>Dynamics 365 メニュー
このツールは **Dynamics 365** メニューを Visual Studio に追加します。 開発プロセス中に使用するいくつかのツールは、ここで入手できます。 たとえば、モデルを管理するツールは、メニューからアクセスします。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

