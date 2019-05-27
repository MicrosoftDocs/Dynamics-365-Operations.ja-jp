---
title: Retail Cloud Scale Unit の初期化
description: このトピックでは、Retail Cloud Scale Unit を初期化する方法について説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 7d51286065d09ed3bb61565c2f9e4763100fd4d2
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537083"
---
# <a name="initialize-retail-cloud-scale-unit"></a>Retail Cloud Scale Unit の初期化

[!include[banner](../includes/banner.md)]

アプリケーション バージョン 8.1.2.x 以降を持つレベル 2 サンドボックスまたは運用環境を使用している場合、販売時点管理 (POS) 操作またはクラウド内の Retail サーバーを使用する電子商取引操作に Retail チャネル機能を使用する前に、Retail Cloud Scale Unit を初期化する必要があります。 初期化は Retail Cloud Scale Unit を展開します。

このトピックでは、Retail Cloud Scale Unit を初期化するための手順について説明します。

## <a name="prerequisites"></a>必要条件

1. アプリケーション バージョン 8.1.2.x またはそれ以降を持つレベル 2 サンドボックスまたは運協環境を配置します。
2. Microsoft Dynamics Lifecycle Services (LCS) で、サポート リクエストを作成し、**Retail Cloud Scale Unit のアクセス権の要求** と入力します。

要求は、5 営業日以内に完了されます。

## <a name="initialize-retail-cloud-scale-unit-as-part-of-a-new-environment-deployment"></a>Retail Cloud Scale Unit を新しい環境の展開の一部として初期化します

1. LCS の環境の詳細 ページで、**環境機能 \> Retail** を選択します。
2. Retail 設定配置ページで、**初期化** を選択します。
3. 初期化する Retail Cloud Scale Unit のバージョンを選択します。
4. Retail Cloud Scale Unit を初期化するリージョンを選択します。

## <a name="configure-retail-channels-to-use-rcsu"></a>RCSU を使用する小売チャンネルを構成します

1. Retail Cloud Scale Unit が展開された後で、本社のクライアントで **Retail > Retail Headquarters > Retail スケジューラの設定 > チャンネル データベース** の順に移動して、この Retail Cloud Scale Unit のためにデータベースを使用するように小売りチャンネルが構成されていることを確認します。
2. 各小売りチャンネルに移動して、対応する Retail Cloud Scale Unit のチャンネル プロファイルを選択します。 

## <a name="deploy-additional-retail-cloud-scale-units-optional"></a>追加の Retail Cloud Scale Unit を展開する (オプション)

最初の Retail Cloud Scale Unit (RCSU) を初期化した後、オプションで RCSU をもうひとつ追加で展開できます。 複数の RCSU が必要な場合は、上限を増やすためにサポート要求の提出が必要で、これには必要な RCSU の数、環境名、そして希望する地域が必要です。

展開する追加の RCSU ごとに、チャネル データ ベースグループを 個別に作成することもお勧めします。 これを行うには、次の手順に従います。 

1. 小売本社で、**Retail > Retail Headquarters > Retail スケジューラーの設定 > チャンネル データベース グループ** の順に移動します。
2. 新しいチャネル データベース グループを作成します。 
3. **Retail > Retail Headquarters > Retail スケジューラの設定 > チャンネル データベース** フォームの順に移動し、新しく作成された RCSU に対応するチャンネル データベースを選択します。 
4. **編集** を選択して、新しいチャンネル データベース グループを選択します。 
5. **保存** を選択します。
6. 選択したチャンネル データベースに対して **完全データ同期の実行** を選択します。

## <a name="additional-considerations-if-you-initialize-cloud-hosted-retail-channel-components-in-an-existing-environment"></a>既存の環境でクラウドにホストされた Retail チャネル コンポーネントを初期化する場合の追加の考慮事項

環境でクラウドでホストされている Retail チャネル コンポーネントを既に使用している場合、Retail Cloud Scale Unit の初期化はそれらのコンポーネントの更新時にダウンタイムを減らすのに役立ちます。 Retail Cloud Scale Unit の初期化を行う前に、追加の計画が必要です。

1. POS のすべてのシフトがクローズしていることを確認してください。
2. すべての P ジョブが正常に完了していることを確認します。
3. すべての POS デバイスからサインアウトします。

Retail サーバーを使用する店舗およびオンライン チャネルのすべての工程で、5 時間のダウンタイム ウィンドウを計画する必要があります。

初期化期間中に実行される内容を以下に示します。

- クラウドでホストされている Retail チャンネルは機能しません (POS オフライン機能がオンの場合を除く)。
- オフライン機能がオンになっている POS デバイスは機能が制限されます。
- Retail サーバーに依存しているすべての電子商取引クライアントが中断されます。
- Retail Store Scale Unit でホストされているチャネルは影響されません。
- 本社機能は影響を受けません。

初期化が完了した後に起きる事柄を示します。

- アクティブ化されたすべての POS デバイスのデバイス有効化状態は保持されます。つまり、デバイスを再有効化する必要はありません。
- スタンドアロン ハードウェア ステーション インスタンスは引き続き機能します。
- POS チャンネル側のレポートはリセットされ、データを初期化する前に表示されません。
- 仕訳帳の処理の表示もリセットされるため、初期化前のデータは表示されません。
