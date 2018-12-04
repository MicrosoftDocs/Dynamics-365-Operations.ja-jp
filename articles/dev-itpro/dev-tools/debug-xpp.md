---
title: "Visual Studio で、デバッガーを使用して X++ コードをデバッグする"
description: "このトピックでは、Microsoft Visual Studio のデバッグ機能を使用して X++ コードをデバッグする方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 23921
ms.assetid: 6be739c0-30da-4f91-97be-a8764fb8078c
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: a20c9a41bb9dca10b5ba6f45be96b36140a31345
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="debug-x-code-by-using-the-debugger-in-visual-studio"></a>Visual Studio で、デバッガーを使用して X++ コードをデバッグする

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Visual Studio のデバッグ機能を使用して X++ コードをデバッグする方法について説明します。 

X++ コードをデバッグするには、Microsoft Visual Studio でデバッガを使用します。 このプロセスは、Visual Studio で作成される他のアプリケーションで使用されるプロセスに似ています。 たとえば、コードがブレークポイントで停止するときに、アプリケーションを検証する標準のツールを使用できます。

## <a name="debug-your-code"></a>コードのデバッグ
X++ コードをデバッグするには、次の手順を実行します。

1. Visual Studio で、デバッグする X++ コードを開きます。
2. 停止を実行する行または明細行を検索し、それらの明細行でブレークポイントを設定します。 行にブレークポイントを設定するには、コード エディターの左の列をクリックするか、カーソルがその行にある間に F9 を押します。 赤いドットは、ブレークポイントが設定されていることを示します。 

   [![赤い丸](./media/32_DevoToolsConcept.png)](./media/32_DevoToolsConcept.png)

3. スタートアップ プロジェクトおよびスタートアップ オブジェクトを設定します。 スタートアップ オブジェクトは、任意のフォーム、**main** メソッドを持つ任意のクラス、または任意のメニュー項目にすることができます。 スタートアップ オブジェクトはプロジェクトの **プロパティ** ウィンドウで設定することができます。 または、ソリューション エクスプローラーで要素を右クリックし、その後**スタートアップ オブジェクトとして設定**をクリックします。

   ![スタートアップ オブジェクトとして設定](./media/setasstartupobject.jpg)

4. **デバッグ**メニューで、**デバッグの開始**をクリックします。
5. アプリケーションで、目的のコードを実行させるアクションを実行します。 標準的なアクションには、フォームを開くことが含まれます。 処理は、設定したブレークポイントで停止します。 

   [![実行](./media/33_DevoToolsConcept.png)](./media/33_devotoolsconcept.png)

6. Visual Studio のツールを使用して、アプリケーションを調べます。 たとえば、その値を表示するため、X++ コード内の変数をポイントします。 また、**デバッグ** メニュー上のコマンドを使用してコードを進めることができます。 また、Visual Studio の **Autos** ウィンドウのようなツールは、アプリケーションの状態に関する重要な情報が表示されます。 

   [![ホバー](./media/34_DevoToolsConcept.png)](./media/34_devotoolsconcept.png)

   Finance and Operations に固有の、もう 1 つのツールは情報ログです。 多くの場合、**info()** ステートメントは、アプリケーションの実行中に、ログ ステータス メッセージのコードに追加されます。 これらの情報ログ メッセージは、Visual Studio で直接表示できます。 **表示**メニューで、**情報ログ**をクリックします。 

   [![情報ログ](./media/35_DevoToolsConcept.png)](./media/35_devotoolsconcept.png)

7. アプリケーションのデバッグが終了した後、Finance and Operations を終了します。 Visual Studio はデバッグ モードを終了します。


<a name="additional-resources"></a>その他のリソース
--------

[開発者ホーム ページ](developer-home-page.md)





