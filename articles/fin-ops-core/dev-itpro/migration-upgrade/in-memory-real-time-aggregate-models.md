---
title: Analysis Services キューブから集計モデルへの移行
description: ことトピックでは、どのように、メモリ内、リアルタイム集計モデルが解析に使われ、なぜ Server Analysis Services (SSAS) キューブの使用から移行したのかを説明します。
author: MilindaV2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 24511
ms.assetid: 877db646-da4b-48b5-83ab-61ae59d91921
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5b0a2f33537c1faf0b504dc79be4a3f969a66a23ce8068afc332f065307c89e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775258"
---
# <a name="transition-from-analysis-services-cubes-to-aggregate-models"></a>Analysis Services キューブから集計モデルへの移行

[!include [banner](../includes/banner.md)]

ことトピックでは、どのように、メモリ内、リアルタイム集計モデルが解析に使われ、なぜ Server Analysis Services (SSAS) キューブの使用から移行したのかを説明します。

世界は、リアルタイムの積極的な分析に移行しています。 履歴データのレポートとトレンドは、最新の視覚化およびプロアクティブ ガイダンスにより置き換えられます。 メモリ内でのリアルタイムな集計モデルにより、分析に以前使用された分析視点が置換されます。

## <a name="a-historical-look-at-perspectives-and-cubes"></a>分析視点とキューブの履歴
Finance and Operations のユーザー エクスペリエンスで重要な役割を果たす埋め込みインサイトを想定しています。 このビジョンにより、製品内に分析機能を構築するための投資が行われました。 Dynamics AX 4.0 では、*分析視点* の概念を導入しました。 目的は、特にレポートのためにモデル化された、ERP スキーマのより簡単なビューを提示することでした。 このより単純なビューは、分析視点と呼ばれていました。 Dynamics AX 4.0 では、システムが、SQL Server レポート ビルダーでアドホック レポートを作成できるレポート モデル (SMDL モデル) を生成していました。 Dynamics AX 2009 では、分析視点でメタデータ定義を使用して、SQL Server Analysis Services (SSAS) プロジェクトを生成する機能を追加しました。 これらのプロジェクトは、SSAS サーバーに展開するとキューブになります。 Dynamics AX 2012 では、分析視点でのモデリングと、SSAS プロジェクトのライフ サイクルを管理するためのツール サポートが向上しました。 データを参照し、Dynamics AX 2012 のキューブでレポートを作成するには、Excel のほか Power View も使用することができました。 SMDL テクノロジも使用されなくなりました。 Dynamics AX 2012 では、SMDL モデルを生成しなくなりました。

## <a name="how-perspectives-are-used-now"></a>現在分析視点がどのように使用されているか
開発者として、システムとの「契約」は視点でした。 システムは、最終目標を達成するのに役立つ「もの」を生み出しました。 Dynamics AX 2012 では、生成された "もの" は SSAS プロジェクトでした。 したがって、あなた (開発者) とシステム (BI フレームワーク) の間の契約は次のとおりでした。

-   分析視点をモデル化しました。
-   システムは、ビジュアルとレポートを作成するために必要な「もの」を生成しました。

分析視点は、Visual Studio のアドインを使ってモデル化されるようになりました。 (Visual Studio は開発環境になっています。) 分析視点は *集計の測定* および *集計分析コード* から構成されます。 開発者は、集計の測定と集計分析コードを使用して業務質問に答えるための簡単なスキーマをモデル化することができます。 集計測定は  Finance and Operations フォームにデータ ソースとして直接バインドできるデータ エンティティ (*集計データ エンティティ* と呼ばれる) を定義することができます。 集計データ エンティティは に使用することもできます

-   PowerBI にデータを公開します。
-   AXQuery オブジェクトを使用してプログラムでデータにアクセス。

[![how-perspectives-are-used。](./../media/how-perspectives-are-used.png)](./../media/how-perspectives-are-used.png)  





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]