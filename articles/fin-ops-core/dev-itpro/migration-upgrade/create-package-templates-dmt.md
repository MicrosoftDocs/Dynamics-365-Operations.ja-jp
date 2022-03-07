---
title: AX 2009 の移行 - パッケージ テンプレートの作成
description: このトピックでは、Microsoft Dynamics AX 2009 から Finance and Operations へデータを移行するために使用できるパッケージ テンプレートを作成する方法について説明します。
author: kfend
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: b4f7d3ee446cad0167d9c48cf935fffd166e4598a6411942b117e8f2769b7e93
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745840"
---
# <a name="ax-2009-migration--create-package-templates"></a>AX 2009 の移行 － パッケージ テンプレートの作成

[!include [banner](../includes/banner.md)]

パッケージを作成するには、事前に定義された順序に従います。 この順序は、データ エンティティが互いに持つ依存関係に基づいています。 これらの依存関係のため、データ エンティティをインポートする場合、定義されている順序でデータ エンティティをインポートする必要があります。 そうしないと、インポートおよびコンフィギュレーション中に問題が発生する可能性があります。

データ移行ツール (DMT) には、次の図に示すように、20 の事前に定義されたテンプレートが用意されています。

[![データ エンティティ インポート テンプレートの一覧。](./media/data-entity-templates.png)](./media/data-entity-templates.png)

既存のテンプレートをカスタマイズできます。または、必要に応じて、独自のテンプレートを作成することができます。

この手順に従って、移行用のテンプレートで使用されるエンティティの一覧を表示して選択します。

1. Microsoft Dynamics AX 2009 で、**データ移行** \> **共通フォーム** \> **エンティティ リスト** を順にクリックしてから、**順序の適用** をクリックします。 メッセージ ボックスを閉じます。
2. 正しい法人が選択されていることを確認し、**表示** フィールドで、すべてのエンティティまたは移行のために考慮すべきエンティティのみのいずれを表示するかを選択します。
3. **テンプレート名** フィールドで、テンプレートを選択します。
4. **選択されているモジュール** ウィンドウで、移行するデータ エンティティを含むモジュールを選択します。
5. **エンティティの詳細** タブで、移行するすべてのエンティティ行の **移行対象として選択** チェック ボックスをオンにします。
6. **順序の適用** をクリックします。
7. カスタマイズされたテンプレートを作成するには、アプリケーション オブジェクト ツリーで、**リソース** に移動し、XML 形式で新しいテンプレートを作成します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]