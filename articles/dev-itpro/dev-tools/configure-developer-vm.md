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
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 23361
ms.assetid: 09dbb06c-dbc7-468d-a78e-e89a97a59fe6
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32a259f093f3788d1f7c16795acf8ccb85fcc93b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369551"
---
# <a name="configure-one-box-development-environments"></a>1 ボックス開発環境の構成

[!include [banner](../includes/banner.md)]

この記事では、ワンボックス開発環境の推奨構成について説明します。

<a name="setup"></a>セットアップ
-----

1. Visual Studio を起動し、ツール バーで <strong>Dynamics 365 **&gt;**オプション</strong>をクリックします。
2. **Microsoft Dynamics** ノードを展開し、**プロジェクト**をクリックします。
3. <strong>要素タイプ別のプロジェクトを整理する</strong> チェック ボックスが選択されていることを確認し、*<strong><em>OK</em></strong>* をクリックします。
4. コード エディターで行番号を表示するには、**ツール**&gt;**オプション**&gt;**テキスト** **エディター**&gt;**すべての言語** を選択します。
5. **行番号** チェック ボックスをオンにします。



## <a name="debugging"></a>デバッグ
より良い X++ デバッガーのパフォーマンスについては、IntelliTrace をオフにすることができます。 IntelliTrace はアプリケーションの完全な実行履歴を収集します。 アプリケーション スイートのような大規模なパッケージをデバッグする場合、X++ デバッグをサポートしておらず、IDE でパフォーマンスの問題が発生します。 Intellitrace をオフにするには、**オプション**&gt;**IntelliTrace**&gt;**IntelliTrace を有効にする** をクリックしてチェック ボックスをオフにし、**OK** をクリックします。 Intellitrace は Visual Studio 2015 の Enterprise 版でのみ使用できることに注意してください。    



