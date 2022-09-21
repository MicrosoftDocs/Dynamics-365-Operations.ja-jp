---
title: Dynamics 365 Human Resources 10.0.30 (2022 年 11 月) の新機能および変更された機能
description: この記事では、Microsoft Dynamics 365 Human Resources バージョン 10.0.30 プレビュー リリースの新機能または変更された機能について説明します。
author: twheeloc
ms.date: 09/02/2022
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
ms.openlocfilehash: 65a64ac77b996e8180447f5601b27aa29299ba6a
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445992"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-10030-november-2022"></a>Dynamics 365 Human Resources 10.0.30 (2022 年 11 月) の新機能および変更された機能

[!include [banner](../../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Human Resources バージョン 10.0.30 の新機能または変更された機能について一覧表示します。 このバージョンのビルド番号は 10.0.1362 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 9 月
- **リリースの一般提供 (手動更新):** 2022 年 10 月
- **リリースの一般提供 (自動更新):** 2022 年 11 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| フィーチャー名 | 開始する | リリース状態 |
|----|----|----|
| 作業者ヘッダー コントロール | Dynamics 365 Human Resources は、**従業員セルフ サービス**、**People** ハブ、合理化された **作業者** ページで、カスタマイズ可能なヘッダー コントロールを提供します。 ヘッダーには、作業者に関する重要な情報と、メール、通話、メッセージングなどの 1 回のクリックによるアクションが含まれます。 ヘッダーを変更するには、フィールドを削除するか、カスタム フィールドを含むフィールドを追加して、追加情報を表示します。 | プレビュー |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) には記載されません。

| フィーチャー名 | 詳細 |
|--------------|------------------|
| タスク管理 | ライブラリのタスクに対する編集は、複数のチェックリストに同時に適用できます。 |

## <a name="known-issues"></a>既知の問題

| 問題の概要 | 詳細 |
| ---- | ---- | 
| タスク管理のアップグレード | 10.0.30 のリリースでは、複数のチェックリストに同時にライブラリ タスクに編集を適用するオプションが追加されました。 これらの編集は、タスク ライブラリのタスクとチェックリスト内のタスクの間に既に関係がある場合にのみロール ダウンできます。 10.0.30 リリース前に、ライブラリ タスクがチェックリストに追加されると、関係は作成されません。 タスク ライブラリとチェックリスト タスク間の関係を作成するには、アップグレードが必要です。 このアップグレードは間もなくリリースされます。 イシュー #732960。 |
| **従業員セルフ サービス** を通じて従業員の支払方法を変更した場合、その支払方法が正しく反映されません。 | 従業員が **従業員セルフ サービス** 経由で支払方法を変更した場合、この変更は、現在サインインしているユーザーには反映されません。 問題が修正されました。 |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Human Resources 10.0.30 には、Platform updates が含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.30 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) を参照してください。
