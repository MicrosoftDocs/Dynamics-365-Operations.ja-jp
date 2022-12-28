---
title: Z レポートのデータ調整に関する問題
description: この記事では、Commerce Headquarters でのZレポートのデータ調整でユーザーに発生する可能性がある問題について説明します。 また、将来の発生を防ぐのに役立つ可能性のあるルートの原因とソリューションについて説明します。
author: Shajain
ms.date: 12/06/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 9803134c4c77233e565525e96fd82af293d4c829
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832137"
---
# <a name="issues-with-the-data-reconciliation-of-a-z-report"></a>Z レポートのデータ調整に関する問題

[!include [banner](../../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce headquarters で Z レポートのデータ調整に関する問題が発生した場合に役立つトラブルシューティングのガイダンスを提供します。 データの調整に関連して発生する可能性のある問題、考えられるルートの原因、将来の発生を防ぐのに役立つソリューションについて説明します。

## <a name="description"></a>Description

- Z レポートに表示される金額と計算された明細書に表示される合計とには不一致があります。
- headquarters のトランザクションの行品目の数が正しくないか、トランザクションの明細合計と合計の間に不一致があります。
- headquarters のシフトに表示されるトランザクション数が Z レポートのトランザクション数より少ない。
- 明細書の転記が前のいずれかの理由で失敗しました。

### <a name="root-cause"></a>根本原因

前に記述した現象の最も一般的なルートの原因は、チャンネル データベース内の重複するトランザクション ID の生成です。 重複したトランザクション ID は次の理由で生成できます。

- Modern Point of Sale (MPOS) のローカル データベース ストレージが壊れている。
- MPOS にはオフライン モードのトランザクションがいくつかあるので、オフライン データベースへのアクセス権がないアカウントを使用すると、そのトランザクションが再有効化されます。
- トランザクション ID の生成に関連するカスタマイズに問題があります。

## <a name="resolution"></a>解決策

通常、Commerce は番号順序に依存して連続するトランザクション ID を生成します。 何らかの理由で番号順序が使用されたかどうかをシステムが判断できない場合は、重複するトランザクション ID が生成されます。 

重複するトランザクション ID の問題を修正するには、サポート チケットを作成してトランザクション データを固定できるかどうかを確認します。 headquarters にデータが損失がない場合など、データの修正を行う必要がない場合があります。

この問題を防ぐには、headquarters で **重複するトランザクション ID** 機能を回避するために、新しいトランザクション ID の有効化を有効にする必要があります。 この機能は、Commerce バージョン 10.0.19 で紹介されました。 これにより、各トランザクションに固有のトランザクション ID が作成され、連続するトランザクション ID が作成されるのを防ぐのに役立ちます。 この機能の詳細については、[トランザクション ID の重複の防止](../channel-setup-retail.md#ensure-unique-transaction-ids) を参照してください。
