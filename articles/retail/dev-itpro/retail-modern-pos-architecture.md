---
title: Retail Modern POS (MPOS) アーキテクチャ
description: このトピックでは、POS トポロジについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.assetid: 210953fb-4d5a-49e6-b4db-6f31b3472789
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 223c053e3cada4eb6839cb9a285c41548073be5c
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833736"
---
# <a name="retail-modern-pos-mpos-architecture"></a>Retail Modern POS (MPOS) アーキテクチャ

[!include [banner](../includes/banner.md)]

このトピックでは、POS トポロジについて説明します。

<a name="retail-modern-pos-topology"></a>Retail Modern POS トポロジー
--------------------------

Retail Modern 販売時点管理 (POS) のユーザーは、サポートされているラップトップ、タブレット、および電話上で、さまざまな小売タスクを実行できます。 これらのタスクには、販売取引の処理、顧客の注文の表示、日常業務と在庫の管理、ロール ベースのレポートの表示などが含まれます。 Retail POS およびクラウド POS の両方は Microsoft Dynamics 365 for Retail で使用できます。  Cloud POS は、POS アプリケーションのホストされているバージョンです。 両方の POS クライアントは、業務機能またはデータ処理を実行しません。 すべてのビジネス機能は Retail サーバーにより提供されています。 Retail Modern POS および Cloud POS クライアントは、クラウドに配置される Retail サーバーと通信できます。 Retail Modern POS クライアントは、Hardware Station を使用することで、キャッシュ ドロワー、クレジット カード リーダー、プリンタなどの周辺機器とも通信できます。 ハードウェア ステーションは、店舗内で配置される必要があり、すべての Retail Modern POS クライアントが同じハードウェア ステーションに接続できます。 次の図は、高レベルのトポロジを示しています。 

[![小売トポロジ](./media/retail-topology-1024x606.png)](./media/retail-topology.png)

## <a name="retail-modern-pos-architecture"></a>Retail Modern POS のアーキテクチャ
ビュー、ビュー コントローラー、デバイスのレイヤーは、Retail Modern POS を展開する予定のオペレーティング システム (Windows RTなど) によって異なります。 他のレイヤーは、オペレーティング システムとは独立しています。 これらのレイヤーは、TypeScript のクラスとモジュールを使用して、ワークフローやエンティティなどの Retail Modern POS 機能を実装します。 次の図は、Retail Modern POS のテクニカル アーキテクチャを示しています。 

[![MPOS](./media/mpos.png)](./media/mpos.png)

## <a name="cloud-pos-and-retail-modern-pos-architecture"></a>クラウド POS および Retail Modern POS アーキテクチャ
Cloud POS は、Retail Modern POS のホストされたバージョンであり、特定のデバイスまたは特定のブラウザでレンダリングされる方法のみが異なります。 また、Retail Modern POS は、オフライン モードをサポートしており、したがってローカル CRT です。 その他のネイティブ周辺機器のサポートは、Retail Modern POS に固有です。 

[![CloudPOS および MPOS](./media/cloudpos-and-mpos.png)](./media/cloudpos-and-mpos.png)



