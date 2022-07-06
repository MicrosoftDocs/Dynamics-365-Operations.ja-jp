---
title: Dynamics 365 Human Resources 10.0.28 (2022 年 8 月) の新機能または変更された機能
description: この記事では、Microsoft Dynamics 365 Human Resources バージョン 10.0.28 プレビュー リリースの新機能または変更された機能について説明します。
author: twheeloc
ms.date: 05/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: eb284c09443ab9690400d48174118d70841b1fb2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853120"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-10028-august-2022"></a>Dynamics 365 Human Resources 10.0.28 (2022 年 8 月) の新機能または変更された機能

[!include [banner](../../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Human Resources バージョン 10.0.28 の新機能または変更された機能について一覧表示します。 このバージョンのビルド番号は 10.0.1264 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 5 月
- **リリースの一般提供 (手動更新):** 2022 年 7 月
- **リリースの一般提供 (自動更新):** 2022 年 7 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

現在、このリリースに新しい機能は含まれていません。 ただし、この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) には記載されません。

| 機能名 | 詳細 |
|--------------|------------------|
| **人事管理** ワークスペースに追加されたタスク管理情報 | 従業員カードが更新され、**チェックリストの適用**、**"N"期限切れタスク**、および **"N"タスクを開く** というオプションを含むチェックリスト ボタンを含められるようになりました。 詳細については、[人事ワークスペース](/hr-personnel-personnel-management-workspace#starting-soon)を参照してください。 |
| 複数の報酬レベルを考慮して更新された署名限度のロジック | 複数の報酬レベル機能がオンになっていて、複数の報酬レベルがジョブに割り当てられている場合、最後に修正された報酬レコードが従業員から取得され、署名限度に必要な報酬レベルを決定するために使用されます。 ジョブに割り当てられている報酬レベルが 1 つだけの場合、その報酬レベルが使用されます。 この動作は、複数の報酬レベル機能がオフになっている場合の動作に一致します。 |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Finance 10.0.28 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.28 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
