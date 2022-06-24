---
title: Dynamics 365 Human Resources (2021 年 11 月 19 日) の新機能および変更された機能
description: この記事では、2021 年 11 月 19 日のスタンドアロン Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: marcelbf
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d3e08432a4ce4d73cd67ad839191abe9f6e691a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886076"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Dynamics 365 Human Resources (2021 年 11 月 19 日) の新機能および変更された機能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Microsoft Dynamics 365 Human Resources の新機能、変更された機能または間もなく近日公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース サイクル 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) の概要 を参照してください。

## <a name="in-this-release"></a>今回のリリース

このリリースには、次のバグ修正が含まれています。 変更は、ビルド番号 8.1.4591 に適用されます。

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 この記事が最初に公開された後に、ビルドに加えたバグ修正を含めるために、この記事を更新する可能性があります。

| 問題の番号 | 問題 | Description |
|---|---|---|
| 626178 | **マネージャー セルフ サービス** で作業者タイルにナビゲーションが存在しない | この問題は修正されました。 ナビゲーションでは、**マネージャー セルフ サービス** でレポートの詳細を表示できます。 |
| 632573 | **コース** の保存時に検証エラーがない | この問題は修正されました。 **最小参加者数** を 0 以上に設定してコースを作成した場合、**最大参加者数** が 0 であっても保存されてしまうという問題がありました。 |
| 615955 | 新しい募集要項の場所を作成する際に、エラー: 「フィールドの **目的** は必ず入力してください」が表示されます。 | 新しい募集要項の場所を作成すると、エラー:「フィールドの目的は必ず入力してください」が表示されます。 ただし、ページで **目的** フィールドを使用できません。 |
| 620797 | **性別** フィールドの空白エラーが誤って発生する | 個人の連絡先に性別が入力されていない場合、レポートに「ここをクリックまたはタップしてテキストを入力してください」と表示されますが、これはフィールドに何も入力できないため誤解を招く可能性があります。 |
| 620800 | 福利厚生明細書のリンクが非表示になる | **従業員セルフサービス** では、既定で福利厚生明細書は表示できません。  **リンク** セクションで **従業員セルフサービス** の右側 にリンクが追加されました |
| 629778 | CDS 統合のパフォーマンスの問題。 | 認証関連のリクエストでパフォーマンスの問題が発生する。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオン/オフにする方法の詳細については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| フィーチャー | リリース計画 | ドキュメント |
|---|---|---|
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>間もなく公開
予定されている機能とリリースの完全な一覧については、[Dynamics 365 とインダストリー クラウド: 2021 年のリリース サイクル 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) の概要 を参照してください。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
