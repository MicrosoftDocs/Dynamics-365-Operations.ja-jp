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
ms.openlocfilehash: 0a81d37324a12d32b55ac89b7479b680d4eb06b1
ms.sourcegitcommit: 31db95d082e33bda06408d0f76bbe44f85c381d2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2022
ms.locfileid: "9594384"
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

## <a name="features-on-by-default-in-this-release"></a>このリリースで、既定で有効になる機能

次の表に、バージョン 10.0.30 で既定で有効になる機能の一覧を示します。 有効にした機能のほとんどは機能管理で自動的にオフにできます。 今後、顧客が最新の機能を確実に使えるよう、自動的に有効にした機能の一部が機能管理から削除され、必須になる可能性があります。 これにより、現在の機能を追加する機能に機能拡張を構築できます。 必要不可欠と判断される場合を除き、1 年未満の機能が自動的に有効になることはありません。 

| フィーチャー名 | 機能の追加日 | 機能状態 | モジュール |
| ---- | ---- | ---- | ---- |
|合理化された従業員の入力|2022 年 3 月 31 日|既定で有効|Human Resources|

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Human Resources 10.0.30 には、Platform updates が含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.30 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) を参照してください。
