---
title: POS 拡張パッケージ情報の表示
description: このトピックでは、販売時点管理 (POS) の設定ビューの拡張パッケージ セクションに関する情報を提供します。 この新しいセクションは、コア POS の一部として含まれる拡張パッケージを一覧表示するとともに、ステータス情報やその他の詳細を表示できます。
author: mumani
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-02-25
ms.dyn365.ops.version: AX 10.0.1
ms.openlocfilehash: 8e13b1415f66be999e90fe94acdaae57b07dc112
ms.sourcegitcommit: 0bd0215d0735ed47b1b8af93a80bcdbf7ca2cc49
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/08/2019
ms.locfileid: "790317"
---
# <a name="view-pos-extension-package-information"></a>POS 拡張パッケージ情報の表示

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]


> [!NOTE]
> このトピックは Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.1 以降、および Microsoft Dynamics 365 for Retail バージョン 10.0.1 以降に適用されます。

販売時点管理 (POS) の **設定** ビューでは、**拡張パッケージ** セクションにコア POS の一部として含まれている POS 拡張パッケージのリストが表示されます。 各パッケージのタイルには、そのパッケージの状態が表示されます。 パッケージの状態は、拡張機能がロードされたのか、ロードできなかったのか、またはスキップされたのかを示します。

## <a name="extension-package-status"></a>拡張パッケージの状態

このセクションでは各パッケージ状態の意味を説明します。

- **読み込み済** – 拡張パッケージが正常に読み込まれました。
- **失敗** – 拡張パッケージが正常に読み込まれませんでした。
- **スキップ** – パッケージはスキップされ、読み込まれませんでした。 拡張マニフェストでパッケージが **en-fr** など特定のロケールに対して読み込まれ、他のすべてのロケールに対してはスキップするよう指定できます。

[![POS 設定ビューの拡張パッケージ セクション](./media/ExtensionPackage.png)](./media/ExtensionPackage.png)

## <a name="extension-package-details"></a>拡張パッケージの詳細

拡張機能のロードで問題が発生した場合、または競合する拡張機能が存在する場合は、それぞれの拡張機能パッケージに提供されている詳細を使用して、どの拡張機能ファイルが問題の原因かを特定できます。 この方法により、問題をトラブルシューティングすることができます。

拡張パッケージの詳細を表示するには、そのパッケージのタイルで **詳細の表示** を選択します。 POS は新しいビューを開き、そこにパッケージの個々の拡張機能すべての詳細が表示されます。 任意の拡張機能が正しく読み込まれなかった場合や、スキップされた場合は、その詳細が右側のペインに表示されます。

**状態** 列はパッケージの各拡張機能の状態を示し、**名前** 列は拡張の種類名を示し、**パス** 列はパッケージの実装ファイルのパスを示します。 特定の行項目を選択すると、右側のウィンドウにも拡張機能の説明が表示されます。

このビューの情報は拡張パッケージに含まれるマニフェスト ファイルに基づいています。 POS 拡張ローダーはすべての拡張パッケージを読み込んで状態を更新します。 状態の情報には記録されたエラーがすべて含まれています。
