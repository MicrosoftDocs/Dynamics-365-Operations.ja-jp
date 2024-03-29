---
title: ウェーブ処理用の倉庫パラメーター
description: この記事では、ウェーブ処理の倉庫パラメーターを設定する方法について説明します。 ウェーブ処理を使用すると、複数作業オーダーのピッキング作業を 1 つのウェーブにグループ化できます。
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e02cd80a3b7692f496fc70e50b812fae358103bc
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067854"
---
# <a name="warehouse-parameters-for-wave-processing"></a>ウェーブ処理用の倉庫パラメーター

[!include [banner](../includes/banner.md)]

この記事では、ウェーブ処理の倉庫パラメーターを設定する方法について説明します。 ウェーブ処理を使用すると、複数作業オーダーのピッキング作業を 1 つのウェーブにグループ化できます。

作業処理を使用するには、**倉庫管理パラメータ** ページで次を指定します。

- バッチ ジョブを使用してウェーブを処理するかどうか。
- ウェーブが処理されるときのログ ファイルの情報を集めるかどうか。

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a>ウェーブ処理の倉庫管理パラメーターの設定

ウェーブ処理の倉庫パラメーターを設定するには、次の手順に従います。

1. **倉庫管理** \> **設定** \> **倉庫管理パラメーター** の順に移動します。

1. **ウェーブ処理** クイック タブで、次の設定を行います。

    - **ウェーブ処理バッチ グループ** - バッチ ジョブを使用してウェーブを処理するときに使用する、バッチ グループを選択します。 バッチ グループは、バッチ ジョブを実行するサーバーを指定します。
    - **バッチでウェーブの処理** - バッチ ジョブでウェーブを自動処理を有効にするかどうかを選択します。 並列処理を使用するには、このオプションを *はい* に設定する必要があります。 **ウェーブの処理** ページでバッチ ジョブで設定します。 (この一覧の最後にある注記も参照してください。)
    - **ウェーブの処理ログを作成する** - 品目の配賦が開始および終了するごとにログ レコードを生成するかどうかを選択します。 このログは、最初のテスト中やトラブルシューティング時など、必要な場合にのみ有効にしてください。 詳細については、[ウェーブ配賦](wave-allocation-method.md) を参照してください。
    - **ウェーブ処理履歴ログを作成する** - 保留中の配賦の並行処理中など、ウェーブの処理後にログ ファイルのウェーブに関する情報を自動的に保存するかどうかを選択します。 通常、間接費が追加されるので、この機能はトラブルシューティングにのみ有効にしてください。 ログを表示するには、**倉庫管理 \> 出荷ウェーブ \> ウェーブ処理履歴ログ** の順に移動します。 ウェーブ処理の詳細については、[ウェーブの作成および処理](wave-processing.md) を参照してください。
    - **コンテナー詰め履歴ログの作成** - ウェーブの処理後に、ログ ファイル内のウェーブに対するコンテナー詰めに関する情報を自動的に保存するかどうかを選択します。 ログを表示するには、**倉庫管理 \> 梱包およびコンテナー詰め \> コンテナー詰め履歴** の順に移動します。
    - **ロックを待機 (ミリ秒)** - 配賦ステップが、他の配賦ステップでロックされたシステム リソースを待機する時間を、ミリ秒単位で入力します。 この時間を超えた場合、ウェーブは処理されず、エラー メッセージが表示されます。

1. **倉庫にリリース** クイック タブで、次の設定を行います。

    - **バッチ失敗のエラー** - 倉庫バッチ ジョブへのリリースが失敗した場合にエラーを生成するかどうかを選択します。 これを有効にすると、失敗したジョブの状態が *エラー* になります。 これを無効にすると、失敗したジョブの状態が *終了* になります。

> [!NOTE]
> ウェーブ処理に使用するウェーブ テンプレートで、ウェーブ処理を自動化する設定を指定できます。 バッチ ジョブのスケジュールを設定する場合、ウェーブ テンプレートの自動化の設定でタイミングを調整する必要があります。 詳細については、[ウェーブ テンプレートの作成](wave-templates.md) を参照してください。
>
> *輸送管理* と *倉庫管理プロセス (WMS)* を使用する場合、ウェーブ処理時に積荷を連結するかどうか指定できます。 たとえば、複数の小さな積荷を同時に出荷するときに便利です。 ファイルを処理するときに負荷を連結するには、**積荷** タブで、**ウェーブ処理中に積荷を連結** チェック ボックスをオンにします。</P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a>生産ウェーブの完全または部分引当の設定

販売注文とかんばん注文では、棚卸資産は注文が倉庫にリリースされる前に引当する必要があります。 そうしなければ、品門行または配賦行はウェーブで処理することはできません。 ただし、製造オーダーはもう少し柔軟です。 製造オーダーでは、以下を指定できます。

- すべての材料を引当することができなくても、製造オーダーが倉庫にリリースされるようにします。 このオプションを選択する場合、追加の材料が使用可能になるときに、倉庫プロセスに手動でリリースを繰り返す必要があります。 たとえば、生産を開始する必要がある材料があり、追加の材料が利用可能になるまで待機できる場合に役立ちます。
- 注文が倉庫にリリースされる前に、すべての材料が引当される必要があります。

完全引当を要求、または部分引当を許可するには、次の手順に従います。

1. **生産管理** \> **設定** \> **生産管理パラメーター** の順に移動します。
1. **全般** タブの **倉庫にリリース** フィールドで、既定の設定を選択します。
