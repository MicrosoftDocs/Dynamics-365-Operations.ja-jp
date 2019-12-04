---
title: Power Apps ホスト コントロール
description: Power Apps ホスト コントロールを使用することにより、作成した PowerApps アプリまたは共有  Power Apps アプリを埋め込むことができます。
author: TLeforMicrosoft
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 16061
ms.assetid: 80c93e91-1952-44ce-af93-a17965ee476a
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2017-04-26
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96165ef62181219110172603caf83617a15c11c9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769566"
---
# <a name="power-apps-host-control"></a>Power Apps ホスト コントロール

[!include [banner](../includes/banner.md)]

Microsoft Power Apps では、作成したアプリや他のユーザーが作成および共有しているアプリを実行することで組織のデータを管理できます。 アプリは[電話などのモバイルデバイスで実行](https://powerapps.microsoft.com/tutorials/run-app-client/)されます。または、Finance and Operations を起動して、[ブラウザー](https://powerapps.microsoft.com/tutorials/run-app-browser/)で実行できます。 C\# 等のプログラミング言語を学習せずに、多くの種類のアプリを作成することができます。 Microsoft Visual Studio を使用する開発者が利用できる Power Apps ホスト コントロールを使用すると、作成した Power Apps アプリまたは共有 Power Apps アプリを埋め込むことができます。 Power Apps の詳細については、[https://powerapps.microsoft.com](https://powerapps.microsoft.com/) を参照してください。

## <a name="host-a-power-apps-app-on-a-page"></a>ページの Power Apps アプリをホストする

1.  Power Apps で、ホストする Web ベースの Power Apps アプリを見つけ、**アプリ ID** 値を記録またはコピーします。
  
    ![Power Apps アプリ ID](media/powerapps-appid.png)
  
2.  Visual Studio でプロジェクトを開き、フォーム デザイナーで、Power Apps ホスト コントロールのインスタンスをページに追加します。
3.  **プロパティ** ウィンドウに**アプリ ID** の値を入力します。
4.  ページで  Power Apps アプリが現在のデータ ソースを共有、またはそこにリンクされている場合、Power Apps アプリで表示するデータのプライマリまたはリンクされたキー フィールドの ID を渡す必要があります。 この場合、ID を**エンティティ ID**、**エンティティ ID データ ソース/フィールド**、または **DataMethod** プロパティの値で指定します。 この値は、 Power Apps アプリに parm 値として渡され、Power Apps アプリはその値を使用して、リンクされているデータを取得する必要があります。 
    
    ![Power Apps ホスト コントロールのプロパティ ウィンドウ](media/powerapps-properties.png)
    
5.  場合によっては、Microsoft によって提供される開発またはサンドボックス Power Apps 環境で Power Apps アプリをホストする場合があります。 この場合、**Power Apps 環境のオーバーライド** プロパティの値としてそのオーバーライド URL を指定する必要があります。

サイズは、コントロールを配置したコンテナーによって決定されます。 使用可能なスペースが限られているフォーム パターンでコントロールを配置し、Power Apps アプリケーションが使用可能領域よりも大きく設計されている場合、Power Apps アプリケーションにスクロール バーが表示されるようになります。
