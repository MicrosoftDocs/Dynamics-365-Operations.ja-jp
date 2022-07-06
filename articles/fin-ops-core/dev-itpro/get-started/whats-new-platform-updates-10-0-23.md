---
title: 財務と運用アプリのバージョン 10.0.23 (2022 年 1 月) のプラットフォーム更新プログラム
description: この記事では、財務と運用アプリのバージョン 10.0.23 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。
author: sericks007
ms.date: 12/10/2021
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2021-10-31
ms.openlocfilehash: 03eb8fb71765237ec0ddf5d3445a6c9b1c18b0f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866629"
---
# <a name="platform-updates-for-version-10023-of-finance-and-operations-apps-january-2022"></a>財務と運用アプリのバージョン 10.0.23 (2022 年 1 月) のプラットフォーム更新プログラム

[!include [banner](../includes/banner.md)]

この記事では、財務と運用アプリのバージョン 10.0.23 のプラットフォーム更新プログラムに含まれる機能の一覧を表示します。 このバージョンのビルド番号は 7.0.6206 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 10 月
- **リリースの一般提供 (セルフ更新)**: 2021 年 12 月
- **リリースの一般提供 (自動更新):** 2022 年 1 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。

| 機能領域    | フィーチャー | 詳細 |  に  によって有効化 |
|-----------------|---------|------------------|---------------------------|
| クライアント機能  | <p>**新しいウィンドウで添付ファイルを開く**</p><p>ユーザーが、**添付ファイル** ページからではなく、新しいウィンドウで添付ファイルを開く場合があります。 これは、添付ファイルが SharePoint に格納されている場合に特に有効で、新しいページで添付ファイルを開くことでユーザー セッションがリセットされるのを防ぐことができます。</p>  | [ドキュメント管理のコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md)  |  **ドキュメント管理パラメータ** ページのオプション |
| クライアント機能  | <p>**グリッド列をコンテンツに合わせて自動でサイズ変更**</p><p>Microsoft Excel と同様に、**新しいグリッドコントロール** 機能が有効になっているユーザーは、列のサイズ調整ハンドルをダブルクリックして、その列の現在の内容に合わせて自動的に列をサイズ変更できます。</p>  | [グリッド機能](../../fin-ops/get-started/grid-capabilities.md)  | [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md)で既定で有効になっている、**新しいグリッド コントロール** 機能に含まれます。  |

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Microsoft Dynamics の Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874&dbType=3&qc=9b7e01944eb8b43f9c3aac4be26811c27be205847d6d2a240424f34f7e722910) を参照してください。

### <a name="dynamics-365-2021-release-wave-2-plan"></a>Dynamics 365: 2021 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2021wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-platform-features"></a>削除済みおよび非推奨のプラットフォーム機能

[削除済みまたは非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md)の記事では、削除された機能、または財務と運用アプリのプラットフォーム更新プログラムで削除予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能を削除する 12 か月前に、[削除または非推奨のプラットフォーム機能](removed-deprecated-features-platform-updates.md)の記事に廃止通知が追加されます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。
