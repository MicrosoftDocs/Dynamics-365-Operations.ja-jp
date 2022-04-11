---
title: 環境サービスの再開
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を通じて展開される環境で個々のサービスを再起動する方法について説明します。こ
author: laneswenka
ms.date: 03/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-03-05
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 15506e07221f33f96a93f4c322f62df1fd8003e7
ms.sourcegitcommit: 399d0d3f8e2ebb81b6b9d640365ebe182690bab2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/15/2022
ms.locfileid: "8418655"
---
# <a name="restart-environment-services"></a>環境サービスの再開

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) のサービスの再開機能を使用すると、**セルフサービス** タイプの階層 2、階層 3、階層 4、または階層 5 の標準承認テスト (サンドボックス) 環境に関連付けられた個々のサービスを再開することができます。 この機能を使用すると、次のサービスを再起動することができます。

- **財務と運用アプリ**- これには X++ ランタイム関数およびバッチ関数が含まれます。
- **データ管理サービス**- このサービスは、データ インポート/エクスポート サービスとも呼ばれます。
- **Financial Preporting サービス**- このサービスを使用して財務諸表を生成します。 

プロジェクト所有者、組織管理者、または環境マネージャーとして LCS プロジェクトに追加されたすべてのユーザーは、この機能を使用するアクセス許可を持っています。

## <a name="restart-a-specific-service"></a>特定のサービスを再起動する

展開された環境で特定のサービスを再起動するには、次の手順を実行します。

1. LCS で、適切なプロジェクトを開き、サービスを再起動する環境を選択します。
2. **環境の詳細** ページで、**メンテナンス** &gt; **サービスのリセット** を選択します。
3. **サービスを再起動します** ダイアログ ボックスで、再起動するサービスを選択してから **OK** を選択します。

    **環境状態** 値は、サービスが再起動されると更新されます。

4. 更新された状態を表示するには、ページを更新します。

    > [!NOTE]
    > サービスの再起動には数秒しかかからないため、**環境の状態** の値はすでに **配置済み** にリセットされている可能性があります。 再起動が完了すると、エントリが **履歴** ページに追加されます。
    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
