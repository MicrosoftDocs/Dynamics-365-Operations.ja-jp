---
title: 1 ボックス開発環境の構成
description: この記事では、ワンボックス開発環境の推奨構成について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 23361
ms.assetid: 09dbb06c-dbc7-468d-a78e-e89a97a59fe6
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d86d25bafba4d419871e055742b9c108b4df358a
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644849"
---
# <a name="configure-one-box-development-environments"></a>1 ボックス開発環境の構成

[!include [banner](../includes/banner.md)]

この記事では、ワンボックス開発環境の推奨構成について説明します。

<a name="setup"></a>セットアップ
-----

1. Visual Studio を起動し、ツール バーで <strong>Dynamics 365 **&gt;**オプション</strong>をクリックします。
2. **Microsoft Dynamics** ノードを展開し、**プロジェクト** をクリックします。
3. <strong>要素タイプ別のプロジェクトを整理する</strong> チェック ボックスが選択されていることを確認し、*<strong><em>OK</em></strong>* をクリックします。
4. コード エディターで行番号を表示するには、**ツール**&gt;**オプション**&gt;**テキスト** **エディター**&gt;**すべての言語** を選択します。
5. **行番号** チェック ボックスをオンにします。



## <a name="debugging"></a>デバッグ
より良い X++ デバッガーのパフォーマンスについては、IntelliTrace をオフにすることができます。 IntelliTrace はアプリケーションの完全な実行履歴を収集します。 アプリケーション スイートのような大規模なパッケージをデバッグする場合、X++ デバッグをサポートしておらず、IDE でパフォーマンスの問題が発生します。 Intellitrace をオフにするには、**オプション**&gt;**IntelliTrace**&gt;**IntelliTrace を有効にする** をクリックしてチェック ボックスをオフにし、**OK** をクリックします。 Intellitrace は Visual Studio の Enterprise 版でのみ使用できることに注意してください。    



