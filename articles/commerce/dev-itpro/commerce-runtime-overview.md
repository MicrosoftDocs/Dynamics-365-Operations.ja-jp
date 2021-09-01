---
title: Commerce Runtime (CRT) のアーキテクチャおよびコンフィギュレーション
description: この記事では、Commerce Runtime (CRT) のアーキテクチャと構成に関する情報を提供します。
author: AamirAllaq
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom:
- "218654"
- intro-internal
ms.assetid: ac422f7e-bc71-4b42-b8c1-4702c6c18421
ms.search.region: Global
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c9c7e4a4c91a0b5a316373ede3cdf5589e88e68a2a1332424859c227152afc32
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766473"
---
# <a name="commerce-runtime-crt-architecture-and-configuration"></a>Commerce Runtime (CRT) のアーキテクチャおよびコンフィギュレーション

[!include [banner](../includes/banner.md)]

この記事では、Commerce Runtime (CRT) のアーキテクチャと構成に関する情報を提供します。 CRT は、ビジネス ロジックをカプセル化するポータブル .NET ライブラリの集合です。 コマース チャネルのエンジンとして機能します。 

## <a name="commerce-runtime-architecture"></a>Commerce Runtime アーキテクチャ

次の図は、Microsoft Dynamics 365 Commerce Runtime (CRT) のコンポーネントを示しています。 

[![Commerce Runtime のコンポーネント。](./media/crt-architecture-1024x793.jpg)](./media/crt-architecture.jpg)

### <a name="data-access"></a>データ アクセス

データベースの上は、データ アクセス レイヤーです。 データ アクセス レイヤーでは、生データがメモリ内のオブジェクトに変換されます。 たとえば、オブジェクトは、製品である可能性があります。 製品は、価格や色などの属性を持ちます。 データ アクセス レイヤーには、オブジェクトを操作するための機能があります。 ストアド プロシージャは、サービスとワークフローで使用できるデータ エンティティにデータベースからデータのパケットを渡します。 データのパケットを更新して、コマースに追加する新しいフィールドを含めることができます。

### <a name="services"></a>サービス

データ アクセス レイヤーの上は、サービス レイヤーです。 リアルタイム データのクエリを処理します。 これらのサービスを使用して、既存の機能をカスタマイズしたり、新しい機能を含む独自のサービスを追加することができます。

### <a name="workflows"></a>ワークフロー

サービス レイヤーの上は、ワークフロー レイヤーです。 ワークフローは、業務プロセスを定義するサービスとビジネス ロジックの集合です。 たとえば、顧客がカートに品目を追加すると、価格の取得、検証の実行、在庫数量の確認、出荷費用の計算、税計算、および割引計算をするためワークフローを使用できます。 コマースに含まれているワークフローを使用することも、新しいワークフローを作成することもできます。 ワークフローを使用して、業務プロセスの一部としてサードパーティ製システムに接続することもできます。

### <a name="api"></a>API

ワークフロー レイヤーーの上は、アプリケーション プログラミング インターフェイス (API) レイヤーです。 項目に関する情報の取得、価格の計算、配送料の計算、および発注などのタスクのために API を使用することができます。 業務プロセスに合わせて API を拡張することができます。

## <a name="commerce-runtime-configuration"></a>Commerce Runtime のコンフィギュレーション

サービスは、CRT コンフィギュレーション ファイルのタイプとして列挙されます。 タイプを CRT 構成ファイルに追加して、どのサービスが CRT に読み込まれるかコントロールすることができます。 コンフィギュレーション ファイルに一覧表示された順序でサービスが読み込まれます。 すべての既定サービスは自動的に読み込まれます。 ただし、既定のサービスのいずれかの上に新しいサービスを追加する場合、新しいサービスは既定のサービスに置き換えられます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
