---
title: Lifecycle Services (LCS) の削除済み、または非推奨の機能
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) から削除された、または削除される予定の機能について説明します。
author: AngelMarshall
manager: AnnBe
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 96ecd040ef8661765c0a3861d8e07fee3c241161
ms.sourcegitcommit: fb7d0efd97754f1ae0b5aa765d0eeb3f57b8078f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027983"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) の削除済み、または非推奨の機能

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) の削除済み、または非推奨の機能について説明します。

- *削除された*フィーチャーはサービスではもう使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

このリストは、自身の計画を立てる際に、これらの削除や非推奨を検討できるように提供されます。

## <a name="october-2019-announcements"></a>2019 年 10 月の発表

### <a name="flowchart-diagrams-in-business-process-modeler"></a>ビジネス プロセス モデラーのフローチャートの図

<table>
<tbody>
<tr>
<td><strong>廃止 / 削除の理由</strong></td>
<td>レガシ デザインによって使用率が低くなったため、ビジネス プロセス モデラ― (BPM) のフローチャート図コンポーネントを廃止しています。</td>
</tr>
<tr>
<td><strong>別の機能での置き換え?</strong></td>
<td>いいえ</td>
</tr>
<tr>
<td><strong>影響を受ける領域</strong></td>
<td>ビジネス プロセス モデラー</td>
</tr>
<tr>
<td><strong>ステータス</strong></td>
<td>非推奨: BPM のフローチャート図コンポーネントは、2020 年に削除されることが予想されます。 次の機能は削除されます。
<ul>
<li>既存のフローチャートを表示したり編集したりすることはできません。 <strong>フローチャート</strong> タブ全体が削除されるため、フローチャート アクティビティに関連付けられている図形プロパティも使用できません。 これらのフローチャートには、自動生成される既定のフローチャートと、既定のフローチャートに基づいて変更されるカスタマイズ フローチャートの両方が含まれます。</li>
<li>レガシ フィット/ギャップ分析機能は使用できません。 したがって、ギャップ リストは自動的に作成されず、エクスポートすることもできません。
<p><strong>注記:</strong>この機能は以前に廃止され、Microsoft Azure DevOps 統合によって置き換えられました。</p>
</li>
<li>フローチャートのバージョン履歴は使用できません。</li>
</ul>
</td>
</tr>
</tbody>
</table>
