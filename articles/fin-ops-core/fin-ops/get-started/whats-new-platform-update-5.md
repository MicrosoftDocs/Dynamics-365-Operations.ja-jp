---
title: Dynamics 365 for Operations プラットフォーム更新プログラム 5 (2017 年 3 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 5 の新機能または変更された機能について説明します。 このバージョンは 2017 年 3 月にリリースされ、ビルド番号は 7.0.4475.16165 です。
author: tonyafehr
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: 273193
ms.assetid: 025acbbf-7c05-407c-bed2-cde1935e11c9
ms.search.region: Global
ms.author: tfehr
ms.dyn365.ops.version: Platform update 5
ms.search.validFrom: 2017-03-31
ms.openlocfilehash: 5e103c3acc2f9fb725ed286dc83a85113cd623c1
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692856"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-platform-update-5-march-2017"></a>Dynamics 365 for Operations プラットフォーム更新プログラム 5 (2017 年 3 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 5 の新機能または変更された機能について説明します。 このバージョンは 2017 年 3 月にリリースされ、ビルド番号は 7.0.4475.16165 です。

## <a name="development-and-customization"></a>開発とカスタマイズ

| 機能 | これが重要である理由 |
|---------|-----------------------|
| 要求または応答シナリオの EventHandlerResult クラス | デリゲート (イベント) ロジックがサブスクライブ (イベント ハンドラー) を必要とするシナリオに対して EventHandlerResult クラスを使用して、複数のサブスクライブおよび複数の結果があるときに結果が失われないようにするため、少なくとも 1 つの応答を提供できるようになりました。 |
| カスタマイズ分析のレポート (CAR) の妥当性 | ベスト プラクティス警告をモデルの AxIgnoreDiagnosticList フォルダーの抑制ファイル内に抑制し、妥当性を含める場合、妥当性テキストがモデルの CAR レポートに表示されます。 妥当性を含む抑制ファイルの例については、&lt;パッケージ ローカル ディレクトリ&gt;\\ディレクトリ\\ディレクトリ\\AxIgnoreDiagnosticList\\ディレクトリ\_BPSuppressions.xml を参照してください。 |
| テレメトリ | モデルが構築されると、テレメトリ フレームワークが、顧客と ISV コードによって参照される Microsoft のクラスおよびメソッドに関する情報を収集します。 これにより、標準アプリケーション コードのどの部分が下位互換性要件に含まれているかに関する多くの必要な情報が Microsoft に提供されます。 |
| X++ コンパイラおよび try catch ブロック | これで、X++ コンパイラは、try catchブロック用のわずかに異なるコードを生成します。 以前、システムは DuplicateKey と UpdateConflict 例外を catch all 句の一部としてキャッチしていました。 これは、取引が実行されているときに try catch が使用された場合、最終的にデータの整合性の問題の原因となる可能性のある問題が発生しました。 ここで、示された 2 つの例外は実行中のトランザクションをロールバックしないため特別であり、catch すべてで取得されなくなります。 詳細については、 ブログ投稿の [X++、Catch](https://blogs.msdn.microsoft.com/mfp/2016/11/24/x-the-catch/) を参照してください。 |

## <a name="personalization"></a>個人用設定

| 機能 | これが重要である理由 |
|---------|-----------------------|
| パーソナル化の拡張された管理機能 | パーソナル化管理者は、現在、ユーザー グループのフォームのパーソナル化を適用または削除できます。 以前は、個人用設定の管理は一度に 1 人のユーザーのみ可能でした。 詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。 |
