---
title: "クラウドでホストされている Retail チャネル コンポーネントの初期化"
description: "このトピックでは、クラウドでホストされている Retail チャネル コンポーネントの初期化方法について説明します。"
author: AamirAllaq
manager: AnnBe
ms.date: 12/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: b8002c547b4f5e7ca485778af90d5b5293496f79
ms.openlocfilehash: 797706f1411d1608919ee5060d65abd199707d36
ms.contentlocale: ja-jp
ms.lasthandoff: 12/10/2018

---


# <a name="initialize-cloud-hosted-retail-channel-components"></a>クラウドでホストされている Retail チャネル コンポーネントの初期化

[!include[banner](../includes/banner.md)]

アプリケーション バージョン 8.1.2.x 以降を持つレベル 2 サンドボックスまたは運用環境を使用している場合、販売時点管理 (POS) 操作またはクラウド内の Retail サーバーを使用する電子商取引操作に Retail チャネル機能を使用する前に、クラウドにホストされている Retail チャネル コンポーネントを初期化する必要があります。

このトピックでは、クラウドでホストされている Retail チャネル コンポーネントを初期化するための手順について説明します。

## <a name="prerequisites"></a>必要条件

1. アプリケーション バージョン 8.1.2.x またはそれ以降を持つレベル 2 サンドボックスまたは運協環境を配置します。
2. Microsoft Dynamics Lifecycle Services (LCS) で、サポート リクエストを作成し、**クラウドでホストされている Retail チャネル コンポーネントのアクセス権の要求**と入力します。

要求は、5 営業日以内に完了されます。

## <a name="initialize-cloud-hosted-retail-channel-components-as-part-of-a-new-environment-deployment"></a>新しい環境の展開の一部としてクラウドでホストされている Retail チャネル コンポーネントを初期化します。

1. LCS の環境の詳細 ページで、**環境機能 \> Retail** を選択します。
2. Retail 設定配置ページで、**初期化** を選択します。
3. 初期化する Retail チャネル コンポーネントのバージョンを選択します。

## <a name="additional-considerations-if-you-initialize-cloud-hosted-retail-channel-components-in-an-existing-environment"></a>既存の環境でクラウドにホストされた Retail チャネル コンポーネントを初期化する場合の追加の考慮事項

環境でクラウドでホストされている Retail チャネル コンポーネントを既に使用している場合、初期化はそれらのコンポーネントの更新時にダウンタイムを減らすのに役立ちます。 初期化を行う前に、追加の計画が必要です。

1. POS のすべてのシフトがクローズしていることを確認してください。
2. すべての P ジョブが正常に完了していることを確認します。
3. すべての POS デバイスからサインアウトします。

Retail サーバーに依存する店舗およびオンライン チャネルのすべての工程で、5 時間のダウンタイム ウィンドウを計画する必要があります。

初期化期間中に実行される内容を以下に示します。

- クラウドでホストされている Retail チャンネルは機能しません (POS オフライン機能がオンの場合を除く)。
- オフライン機能がオンになっている POS デバイスは機能が制限されます。
- Retail サーバーに依存しているすべての電子商取引クライアントが中断されます。
- Retail Store Scale Unit でホストされているチャネルは影響を受けません。
- 本社機能は影響を受けません。

初期化が完了した後に起きる事柄を示します。

- アクティブ化されたすべての POS デバイスのデバイス有効化状態は保持されます。 したがって、デバイスを再度有効化する必要はありません。
- スタンドアロン ハードウェア ステーション インスタンスは引き続き機能します。
- POS チャンネル側のレポートはリセットされ、データを初期化する前に表示されません。

