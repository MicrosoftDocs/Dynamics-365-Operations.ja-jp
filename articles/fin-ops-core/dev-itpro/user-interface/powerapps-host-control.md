---
title: PowerApps ホスト コントロール
description: PowerApps ホスト コントロールを使用することにより、作成した PowerApps アプリまたは共有  PowerApps アプリを埋め込むことができます。
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
ms.openlocfilehash: 4d18df306b50bb1312f6e6ddf3738a01aab781c0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191765"
---
# <a name="powerapps-host-control"></a>PowerApps ホスト コントロール

[!include [banner](../includes/banner.md)]

Microsoft PowerApps では、作成したアプリや他のユーザーが作成および共有しているアプリを実行することで組織のデータを管理できます。 アプリは[電話などのモバイルデバイスで実行](https://powerapps.microsoft.com/tutorials/run-app-client/)されます。または、Finance and Operations を起動して、[ブラウザー](https://powerapps.microsoft.com/tutorials/run-app-browser/)で実行できます。 C\# 等のプログラミング言語を学習せずに、多くの種類のアプリを作成することができます。 Microsoft Visual Studio を使用する開発者が利用できる PowerApps ホスト コントロールを使用すると、作成した PowerApps アプリまたは共有 PowerApps アプリを埋め込むことができます。 PowerApps の詳細については、[https://powerapps.microsoft.com](https://powerapps.microsoft.com/) を参照してください。

## <a name="host-a-powerapps-app-on-a-page"></a>ページの PowerApps アプリをホストする

1.  PowerApps で、ホストする Web ベースの PowerApps アプリを見つけ、**アプリ ID** 値を記録またはコピーします。
  
    ![PowerApps アプリ ID](media/powerapps-appid.png)
  
2.  Visual Studio でプロジェクトを開き、フォーム デザイナーで、PowerApps ホスト コントロールのインスタンスをページに追加します。
3.  **プロパティ** ウィンドウに**アプリ ID** の値を入力します。
4.  ページで  PowerApps アプリが現在のデータ ソースを共有、またはそこにリンクされている場合、PowerApps アプリで表示するデータのプライマリまたはリンクされたキー フィールドの ID を渡す必要があります。 この場合、ID を**エンティティ ID**、**エンティティ ID データ ソース/フィールド**、または **DataMethod** プロパティの値で指定します。 この値は、 PowerApps アプリに parm 値として渡され、PowerApps アプリはその値を使用して、リンクされているデータを取得する必要があります。 
    
    ![PowerApps ホスト コントロールのプロパティ ウィンドウ](media/powerapps-properties.png)
    
5.  場合によっては、Microsoft によって提供される開発またはサンドボックス PowerApps 環境で PowerApps アプリをホストする場合があります。 この場合、**PowerApps 環境のオーバーライド** プロパティの値としてそのオーバーライド URL を指定する必要があります。

サイズは、コントロールを配置したコンテナーによって決定されます。 使用可能なスペースが限られているフォーム パターンでコントロールを配置し、PowerApps アプリケーションが使用可能領域よりも大きく設計されている場合、PowerApps アプリケーションにスクロール バーが表示されるようになります。
