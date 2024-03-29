---
title: チャネルを別の Commerce Scale Unit に移行する
description: この記事では、Microsoft Dynamics 365 Commerce チャネルを別の Commerce Scale Unit に移行する方法について説明します。
author: jashanno
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: a74d5e8d8a1e1a9c82f6db4e38b536522aad0595
ms.sourcegitcommit: 719600437fc0895efac374f954a895e4c951da6e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736819"
---
# <a name="migrate-channels-to-a-different-commerce-scale-unit"></a>チャネルを別の Commerce Scale Unit に移行する

[!include[banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce ストア チャネルを、現在使用している Commerce Scale Unit (CSU) から別の CSU に移行する方法について説明します。 チャネル間の負荷の分離とリソース ガバナンスの向上のためにチャネルを別の CSU に移行して、店舗への待ち時間を減らしたり、またはロールアウトとパイロットのステージングのために別の更新や拡張機能の展開スケジュールを管理することがあります。 異なる CSU への移行には、チャネルのダウンタイムが含まれます。

この記事では、チャネル移行中の業務の中断とダウンタイムを最小限に抑えるのに役立つベスト プラクティスについて説明します。 これは、クラウドでホストされた CSU 間、自己ホストの CSU 間、クラウドでホストされた CSU から自己ホストの CSU、および自己ホストの CSU からクラウドでホストされた CSU へのチャネルの移行に適用されます。

> [!NOTE]
> 移行の前に、CSU 間、仕訳帳レコードで使用されていた一時的な販売データ、および販売時点管理 (POS) レポートでチャネルを移行すると、移行後は POS で使用できなくなります。 移行が完了した後は、新しいデータを使用して、仕訳帳とチャネル レポートが開始されます。

次の手順において、*出力元* と *出力先* という用語は、移行に含まれる CSU と対応するチャネル データベースを区別するために使用されます。

## <a name="planning-for-downtime"></a>ダウンタイムの計画

この記事で説明する手順に従うと、関連する実行時間の長いシステム プロセスはすべて実際の移行の前に実行されますが、その間、店舗は運営することができます。 これらのプロセスには、製品、価格、および顧客のマスター データの同期が含まれます。 次に、移行中、環境のダウンタイムを計画する必要がある重要な期間には、新しい CSU に対するチャンネル コンフィギュレーション データの小さなペイロードの同期が含まれます。 ほとんどの場合、この同期は 10 分以内に完了することができます。 ただし、運用上の視点から、前提条件となる手順すべてを完了するのに十分な時間があるよう、より長いダウンタイム ウィンドウを計画する必要があります。 この手順には、すべてのシフトのクローズ、Commerce 本社へのトランザクションの同期、およびステートメントの転記が含まれます。 必要な合計時間は組織ごとに異なります。

## <a name="prerequisites"></a>必要条件

最初に、サンドボックスのユーザー受け入れテスト (UAT) 環境で、次のすべての手順を実行します。 次に、運用環境で手順を繰り返します。 このようにして、運用環境で予想されるダウンタイムの測定および見積ができます。

## <a name="migration"></a>移行

### <a name="configure-data-synchronization"></a>データ同期のコンフィギュレーション

次の手順は、店舗がまだ運営中の間に完了することができます。 マスター データを出力先の CSU に同期します。

1. Commerce 本社の **チャネル データベース** ページで、出力先 CSU のチャネル データベースのレコードを選択します。 
2. 目的のチャネルを出力先のチャネル データベースに追加します。
3. **完全なデータの同期** を選択し、ジョブ **9999** (**すべてのジョブ**) を使用するように指定します。

> [!NOTE]
> 出力先の CSU が自己ホストの場合、個別のチャネル データベース グループを作成して、不要なマスター データ同期量を減らすことを考慮してください。 チャンネル データベース グループの構成に関係なく、このドキュメントの手順では、ソース CSU と行先 CSU を含むグループの両方に、以下の実行済みのジョブがすべて含まれます。 たとえば、ソース CSU と行先の CSU が異なるチャネル データベース グループ内にある場合、両方のグループが、実行する必要があるジョブのすべてのインスタンスに対して配送スケジュール ジョブをまとめて実行する必要があります。

### <a name="prepare-for-migration"></a>移行の準備

この手順と次の手順は、チャネルに計画されたダウンタイムの間に完了する必要があります。

1. すべての POS デバイスで、シフトすべてがクローズされていることを確認してください。
2. すべての POS デバイスからサインアウトします。
3. すべての POS オフライン トランザクションが Commerce 本社に同期されていることを確認してください。 移行するすべての既存のチャネル データベースに対して、P ジョブを実行します。 P ジョブが完了する前に移行を開始し、クラウド POS を使用している場合、トランザクション番号が重複するためにトランザクションが失われる可能性があります。
4. すべてのステートメントが転記されることを確認します。

### <a name="migrate-channels-to-a-new-csu"></a>チャネルを新しい CSU に移行する

1. **店舗の詳細** ページで、**ライブ チャネル データベース** フィールドを送信先 CSU データベースに設定します。
2. **チャネル プロファイル** フィールドを、送信先の CSU に関連付けられているチャネル プロファイルに設定します。
3. **配送スケジュール** ページで、ジョブ **1070** ( **チャネル構成ジョブ**) とジョブ **1110** (**グローバル構成ジョブ**) を実行します。 各ジョブに対して **今すぐ実行** を選択します。 (非同期処理については、**今すぐ実行** の代わりに **バッチ ジョブの作成** を選択します。) ジョブが完了した後、チャネルは新しい CSU に移行されています。
4. クラウド POS を使用している場合、新しい CSU のためのクラウド POS の URL を使用して、POS デバイスの最有効化を行う必要があります。 送信元のチャネル データベースのすべての P ジョブが完了する前に POS デバイスの最有効化を実行すると、トランザクション番号が重複するためにトランザクションが失われる可能性があります。

    Modern POS を使用している場合、各 POS デバイスを閉じ、再度開いてサインインします。

## <a name="post-migration"></a>移行後

引き続き、元の CSU を使用して、他のチャネルのサービスを提供することができます。 

> [!NOTE]
> 元の CSU を削除しないでください。 これを行うと、店舗を開けなくなる可能性があります。

サンドボックス UAT 環境ですべての手順を完了した後、運用環境で同じ手順を繰り返します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
