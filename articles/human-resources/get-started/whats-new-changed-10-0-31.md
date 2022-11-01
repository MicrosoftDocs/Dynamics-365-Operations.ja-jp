---
title: Dynamics 365 Human Resources 10.0.31 (2023 年 1 月) の新機能および変更された機能
description: この記事では、Microsoft Dynamics 365 Human Resources バージョン 10.0.31 プレビュー リリースの新機能または変更された機能について説明します。
author: twheeloc
ms.date: 10/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 414ac43665e4ad5bd8bbfd204899049ff2586dd7
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/21/2022
ms.locfileid: "9711569"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-10031-january-2023"></a>Dynamics 365 Human Resources 10.0.31 (2023 年 1 月) の新機能および変更された機能

[!include [banner](../../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Human Resources バージョン 10.0.31 の新機能または変更された機能について一覧表示します。 このバージョンのビルド番号は 10.0.1406 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 10 月
- **リリースの一般提供 (手動更新):** 2023 年 1 月
- **リリースの一般提供 (自動更新):** 2023 年 2 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| 機能名 | 開始する | リリース状態 |
|----|----|----|
| コースの拡張機能 | <p>コースの拡張機能では、次の機能が有効です。</p><ul><li>コースは仮想コースとして指定し、コース リンクを定義できます。</li><li>コースの割り当てには期日を定義できます。</li><li>**従業員セルフサービス**、コース/学習の概要が従業員に表示され、期限が過ぎたコース、期日が近いコース、および割り当てられたコースを従業員に表示できるようになりました。</li><li>従業員は仮想コースを修了し、自己テストを行うことができます。</li></ul><p> | プレビュー |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) には記載されません。

| 機能名 | 詳細 |
|--------------|------------------|
| タスク管理 | これまでは、タスクの更新を行った場合、そのタスクを含む各チェックリストに移動し、タスクを個別に更新する必要がありました。 10.0.30 リリースの変更により、ライブラリ タスクの編集時にチェックリスト タスクを更新するオプションが追加されました。 関連付けられたチェック リストすべてに対して適用された編集については、タスク ライブラリのタスクとチェックリスト内のタスクの間に既にリレーションシップが存在している必要があります。 10.0.30 リリースより前は、リレーションシップの変更が作成されません。 ライブラリ タスクとチェックリスト タスク間の関係を作成するために、アップグレードが作成されました。 |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Human Resources 10.0.31 には、Platform updates が含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.31 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics Lifecycle Services にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525) を参照してください。
