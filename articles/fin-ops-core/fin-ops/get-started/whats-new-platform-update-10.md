---
title: Dynamics 365 for Finance and Operations, Enterprise Edition プラットフォーム更新プログラム 10 (2017 年 8 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations, Enterprise Edition プラットフォーム更新プログラム 10 の新機能または変更された機能について説明します。 このバージョンは 2017 年 8 月にリリースされました。
author: tonyafehr
ms.date: 08/17/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 10
ms.openlocfilehash: 2f6c172f49cb92eb063e3f6b9e8ec6c311c2b1d7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752624"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-enterprise-edition-platform-update-10-august-2017"></a>Dynamics 365 for Finance and Operations, Enterprise Edition プラットフォーム更新プログラム 10 (2017 年 8 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Finance and Operations, Enterprise Edition プラットフォーム更新プログラム 10 の新機能または変更された機能について説明します。 このバージョンは 2017 年 8 月にリリースされ、ビルド番号は 7.0.4641.16233 です。

新機能についての補足情報の検索および開発中の新機能に関する詳細については、[Dynamics 365 ロードマップ](https://roadmap.dynamics.com/) を参照してください。 プラットフォーム更新プログラム 10 に含まれるバグ修正の詳細については、Lifecycle Services (LCS) にログインし、この [サポート技術情報記事](https://go.microsoft.com/fwlink/?linkid=856083) を参照してください。

## <a name="browser-client---net-promoter-score-integration"></a>ブラウザー クライアント - ネット プロモーター スコアの統合

この機能は、ユーザーに Dynamics 365 for Finance and Operations, Enterprise Edition にフィードバックを提供し、満足度をランク付けするよう定期的に促します。

## <a name="browser-client---support-for-keyboard-shortcut-sequences"></a>ブラウザー クライアント - キーボード ショートカット シーケンスのサポート

Dynamics 365 for Finance and Operations, Enterprise Edition は、キーボードのみのユーザーが生産性を高めるために、多数のキーボード ショートカットをサポートする複合的な製品です。 今後の機能のキーボード ショートカットを選択するのに十分な数の選択肢を確保し、同様のアクションのショートカットをグループ化できるように、キー シーケンスがサポートされました。 キーの順序は、2 つのキーの組み合わせを順番に押すことで開始されるように特定のアクションを許可します。 たとえば、キーの順序 (Alt + M、N) は、Alt キーを押しながら M を押し、直後に N キーを押すことで、ナビゲーション バーにフォーカスを移動するための新しいショートカットになります。 製品内のキー シーケンスの他の例、特にタスク レコーダーに関連するアクションのショートカットについては、[キーボード ショートカット](shortcut-keys.md)を参照してください。

## <a name="build-and-maintain-mobile-workspaces-using-x-classes"></a>X++ クラスを使用してモバイル ワークスペースをビルドおよび管理する

このリリースでは、Microsoft Visual Studio の X++ クラスを使用してモバイル ワークスペースを作成および管理するための新しいモデルが導入されました。 これにより、アプリのパフォーマンスを大幅に向上させるだけでなく、開発の柔軟性とパワーを高めることができます。 このモデルでは、開発者はフォームを作成する必要なく複雑なクエリ/構造を作成できます。 プログラムを使用してモバイルのワークスペースにデータを提供するコードを開発および編集することもできます。 結果として、この新しいモデルではモバイル ワークスペースの管理が大幅に改善されています。 アプリケーション デザイナーは、モバイル ワークスペースをすばやく構築するために引き続き貴重なツールであり、モバイル ワークスペースを作成するときに新しいモデルと組み合わせて使用することができます。 詳細については、[モバイル プラットフォーム](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) で「サーバー側の開発」を参照してください。

## <a name="excel-add-in-enables-passing-header-context-to-detail-records"></a>Excel アドインでは、詳細レコードにヘッダー コンテキストを渡すことが可能です。

この機能により、Excel アドインを使用してトランザクション データの作成や編集をしたり、行レコードに加えてヘッダー レコードを作成したりすることにより、ユーザーの生産性が向上します。  たとえば、仕訳帳入力については、仕訳帳の Excel で明細行を開くを使用して、仕訳帳を公開し、Excel で直接新しい仕訳帳を作成します。 これにより、Finance and Operations クライアントに戻る必要がなくなります。 さらに、ユーザーが Excel アドインから期待する生産性リレーショナル ルックアップ体験が、仕訳帳明細行などの関連する明細行レコードと同様に、仕訳帳などのヘッダー レコードに使用できます。 詳細については、[Excel で開くエクスペリエンスの作成](../../dev-itpro/office-integration/office-integration-edit-excel.md) を参照してください。

## <a name="skype-support-for-human-resources-and-retail"></a>人事管理 および小売の Skype サポート

クラウド プラットフォームを使用して開発されたすべてのアプリケーションで Skype 統合が有効になります。 Skype 統合が Finance and Operations アプリで有効にされている間は、人事管理 および小売を含む他のアプリケーションでもこの機能は使用可能です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]