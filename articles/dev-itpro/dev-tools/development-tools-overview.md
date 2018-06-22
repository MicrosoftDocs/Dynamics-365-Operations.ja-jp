---
title: "開発ツールの概要"
description: "Visual Studio 2015 は、単一の開発用統合開発環境 (IDE) です。"
author: robadawy
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 23401
ms.assetid: 
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: baba0f4ee3657477216e5d096560621c7acfce07
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="development-tools-overview"></a>開発ツールの概要

[!include [banner](../includes/banner.md)]

## <a name="what-are-the-development-tools"></a>開発ツールとは
Microsoft Dynamics AX 2012 からの重要な変更は、Microsoft Dynamics 365 for Finance and Operations にリッチ クライアント アプリケーション (ax32.exe) が含まれていないことです。 開発の観点では、Microsoft Dynamics AX 2012 の開発環境、MorphX が使用されなくなることを意味します。 代わりに、アプリケーション開発は Visual Studio でのみ実行されます。 開発ツールは、デバッグおよびローカル テストのシナリオを含むすべての開発タスクをサポートします。 開発経験の主な目的は、使い慣れた Microsoft Dynamics AX 2012 の概念を保持しながら、Visual Studio のフレームワークおよびパラダイムにシームレスに順応することです。

Visual Studio 2015 は、単一の開発用統合開発環境 (IDE) です。 すべてのアプリケーション開発作業がそのアプリケーションで実行されます。 このセクションでは、開発ツールのインストール時に Visual Studio に追加される主な機能の概要を説明します。

### <a name="application-explorer"></a>アプリケーション エクスプローラー
Visual Studio で、モデル ストアはアプリケーション エクスプローラーで表されます。 **表示**メニューで、**アプリケーション** **エクスプローラー**をクリックして開きます。 アプリケーション エクスプローラーは、Microsoft Dynamics AX 2012 をよく理解しているアプリケーション オブジェクト ツリー (AOT) に対応します。 アプリケーション エクスプローラーを使用して、アプリケーションを定義するモデル ストア内の要素を参照および操作します。 次の図は、アプリケーション エクスプローラーを示しています。 詳細については、[アプリケーション エクスプローラー](application-explorer.md) を参照してください。

![アプリケーション エクスプローラー](media/1_devotoolsconcept.png)

### <a name="the-project-template"></a>プロジェクト テンプレート
単純なアプリケーションであっても、そのモデルには多数の要素を含めることができます。 モデルに使用する要素を整理および管理するために、**業務プロジェクト** テンプレートが Visual Studio に追加されました。 このプロジェクトを使用して、モデル要素の設計、作成、およびをテストをします。 1 つの Visual Studio ソリューション内に複数のプロジェクトがあることが一般的です。 次の図は、Visual Studio ソリューションの 3 つのプロジェクトを示しています。 詳細については、[プロジェクト](projects.md) を参照してください。

![ソリューション エクスプローラー](media/2_devotoolsconcept.png)

### <a name="element-designers"></a>要素デザイナー
Visual Studio Tools には、アプリケーション内の要素の種類ごとのデザイナーが含まれています。 要素を作成または変更するときは、これらのデザイナーを使用します。 次の図は、フォーム要素の要素デザイナーを示しています。 詳細については、[要素デザイナー](element-designers.md) を参照してください。

![要素デザイナー](media/3_devotoolsconcept.png)

### <a name="code-editor"></a>コード エディター
X++ コードは、Visual Studio 用のコード エディタに書き込まれます。 開発者がコード エディターに期待する標準機能がサポートされています。 たとえば、コードのセクションは折りたたみ可能です。 IntelliSense は、コードを書き込みまたは変更するガイダンスを提供します。 詳細については、[コード エディター](code-editor.md) を参照してください。

![コード エディター](media/4_devotoolsconcept.png)

### <a name="dynamics-365-menu"></a>Dynamics 365 メニュー
このツールは **Dynamics 365** メニューを Visual Studio に追加します。 開発プロセス中に使用するいくつかのツールは、ここで入手できます。 たとえば、モデルを管理するツールは、メニューからアクセスします。


