---
title: "Commerce Runtime の概要"
description: "この記事では、Commerce Runtime (CRT) のアーキテクチャと構成に関する情報を提供します。 CRT は、ビジネス ロジックをカプセル化するポータブル .NET ライブラリの集合です。 小売チャネルのエンジンとして機能します。"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 218654
ms.assetid: ac422f7e-bc71-4b42-b8c1-4702c6c18421
ms.search.region: Global
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: bcd12129b57c5926a134e5806ee91c3e4da4d208
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="commerce-runtime-overview"></a>Commerce Runtime の概要

[!include [banner](../includes/banner.md)]

この記事では、Commerce Runtime (CRT) のアーキテクチャと構成に関する情報を提供します。 CRT は、ビジネス ロジックをカプセル化するポータブル .NET ライブラリの集合です。 小売チャネルのエンジンとして機能します。 

<a name="commerce-runtime-architecture"></a>Commerce Runtime のアーキテクチャ
-----------------------------

次の図は、Retail Commerce Runtime (CRT) 用の Microsoft Dynamics 365 のコンポーネントを示しています。 

[![コマース ランタイム コンポーネント](./media/crt-architecture-1024x793.jpg)](./media/crt-architecture.jpg)

### <a name="data-access"></a>データ アクセス

データベースの上は、データ アクセス レイヤーです。 データ アクセス レイヤーでは、生データがメモリ内のオブジェクトに変換されます。 たとえば、オブジェクトは、製品である可能性があります。 製品は、価格や色などの属性を持ちます。 データ アクセス レイヤーには、オブジェクトを操作するための機能があります。 ストアド プロシージャは、サービスとワークフローで使用できるデータ エンティティにデータベースからデータのパケットを渡します。 Dynamics 365 for Retail に追加する新しいフィールドを含めるように、データのパケットを更新することができます。

### <a name="services"></a>サービス

データ アクセス レイヤーの上は、サービス レイヤーです。 リアルタイム データのクエリを処理します。 これらのサービスを使用して、既存の機能をカスタマイズしたり、新しい機能を含む独自のサービスを追加することができます。

### <a name="workflows"></a>ワークフロー

サービス レイヤーの上は、ワークフロー レイヤーです。 ワークフローは、業務プロセスを定義するサービスとビジネス ロジックの集合です。 たとえば、顧客がカートに品目を追加すると、価格の取得、検証の実行、在庫数量の確認、出荷費用の計算、税計算、および割引計算をするためワークフローを使用できます。 Dynamics 365 for Retail に含まれているワークフローを使用することも、新しいワークフローを作成することができます。 ワークフローを使用して、業務プロセスの一部としてサードパーティ製システムに接続することもできます。

### <a name="api"></a>API

ワークフロー レイヤーーの上は、アプリケーション プログラミング インターフェイス (API) レイヤーです。 項目に関する情報の取得、価格の計算、配送料の計算、および発注などのタスクのために API を使用することができます。 業務プロセスに合わせて API を拡張することができます。

## <a name="commerce-runtime-configuration"></a>Commerce Runtime のコンフィギュレーション
サービスは、CRT コンフィギュレーション ファイルのタイプとして列挙されます。 タイプを CRT 構成ファイルに追加して、どのサービスが CRT に読み込まれるかコントロールすることができます。 コンフィギュレーション ファイルに一覧表示された順序でサービスが読み込まれます。 すべての既定サービスは自動的に読み込まれます。 ただし、既定のサービスのいずれかの上に新しいサービスを追加する場合、新しいサービスは既定のサービスに置き換えられます。




