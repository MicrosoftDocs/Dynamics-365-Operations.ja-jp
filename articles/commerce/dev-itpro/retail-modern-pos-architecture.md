---
title: Modern POS (MPOS) アーキテクチャ
description: この記事では、POS トポロジについて説明します。
author: josaw1
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 83892
ms.assetid: 210953fb-4d5a-49e6-b4db-6f31b3472789
ms.openlocfilehash: e6a4dd1e240b47bd8f3554475323229197ae4698
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286594"
---
# <a name="modern-pos-mpos-architecture"></a>Modern POS (MPOS) アーキテクチャ

[!include [banner](../includes/banner.md)]

この記事では、POS トポロジについて説明します。

## <a name="modern-pos-topology"></a>Modern POS トポロジ

Modern 販売時点管理 (POS) のユーザーは、サポートされているラップトップ、タブレット、および電話上で、さまざまなタスクを実行できます。 これらのタスクには、販売取引の処理、顧客の注文の表示、日常業務と在庫の管理、ロール ベースのレポートの表示などが含まれます。 MPOS および Cloud POS の両方は Microsoft Dynamics 365 Commerce で使用できます。 Cloud POS は、POS アプリケーションのホストされているバージョンです。 両方の POS クライアントは、業務機能またはデータ処理を実行しません。 すべてのビジネス機能は、Commerce Scale Unit によって提供されます。 Modern POS および Cloud POS クライアントは、Commerce Scale Unit と通信できます。 Modern POS クライアントは、Hardware Station を使用することで、キャッシュ ドロワー、クレジット カード リーダー、プリンタなどの周辺機器とも通信できます。 Hardware Station は、店舗内で配置される必要があり、すべての Modern POS クライアントが同じ Hardware Station に接続できます。 次の図は、高レベルのトポロジを示しています。

![コマース トポロジ。](./media/retail-topology-1024x606.png)

## <a name="modern-pos-architecture"></a>Modern POS のアーキテクチャ

ビュー、ビュー コントローラー、デバイスのレイヤーは、Modern POS を展開する予定のオペレーティング システム (Windows RT など) によって異なります。 他のレイヤーは、オペレーティング システムとは独立しています。 これらのレイヤーは、TypeScript のクラスとモジュールを使用して、ワークフローやエンティティなどの Modern POS 機能を実装します。 次の図は、Modern POS のテクニカル アーキテクチャを示しています。

![Modern POS のアーキテクチャ。](./media/mpos.png)

## <a name="cloud-pos-and-modern-pos-architecture"></a>Cloud POS および Modern POS アーキテクチャ

Cloud POS は、Modern POS のホストされたバージョンであり、特定のデバイスまたは特定のブラウザでレンダリングされる方法のみが異なります。 また、Modern POS は、オフライン モードをサポートしており、したがってローカル CRT です。 その他のネイティブ周辺機器のサポートは、Modern POS に固有です。

![CloudPOS および MPOS。](./media/cloudpos-and-mpos.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
