---
title: Dynamics 365 for Operations プラットフォーム更新プログラム 6 (2017 年 4 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 6 の新機能または変更された機能について説明します。 このバージョンは 2017 年 4 月にリリースされ、ビルド番号は 7.0.4509.16180 です。
author: tonyafehr
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: ''
ms.assetid: 13d2b8a5-c2e0-4f32-a43b-7726ae20392c
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: ''
ms.dyn365.ops.version: Platform update 6
ms.openlocfilehash: 459cb3c270c6de343f82ccf346ac7f4205ae8676
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510854"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-platform-update-6-april-2017"></a>Dynamics 365 for Operations プラットフォーム更新プログラム 6 (2017 年 4 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 6 の新機能または変更された機能について説明します。 このバージョンは 2017 年 4 月にリリースされ、ビルド番号は 7.0.4509.16180 です。

## <a name="browser-framework--powerapps-host-control"></a>ブラウザー フレームワーク - PowerApps ホスト コントロール

Dynamics 365 for Operations は、開発者に対して新しいコントロールである PowerApps ホスト コントロールを導入します。 このコントロールにより、開発者は Dynamics 365 for Operations フォーム内で PowerApp をホストまたは埋め込むことができます。 詳細については、[PowerApps ホスト コントロール](../../dev-itpro/user-interface/powerapps-host-control.md) を参照してください。

## <a name="browser-client--ability-to-model-toolbar-actions-in-the-overflow-menu"></a>ブラウザー クライアント - オーバーフロー メニューのツール バー アクションをモデル化する機能

ツールバー内の特定のボタンを常にオーバーフローで表示するように設計することで、フォーム上に簡潔なアクション ストーリーを提供することができるようになりました。 これにより、ユーザーが頻繁に使用する操作と、まれにしか使用されない操作とを区別することが容易になります。 この機能を利用するには、ツールバー内にあるボタン グループの新しい **AlwaysInOverflow** メタデータ プロパティを試してください。

## <a name="build-automation--automatic-update-of-model-version-during-build"></a>ビルド自動化 - ビルド中のモデル バージョンの自動更新

自動ビルド中に、ビルド中のモデルのバージョンが更新され、ビルド番号が反映されます。 これにより、お客様は、Azure DevOps のビルド履歴に戻り、Dynamics 365 for Operations ウィンドウのモデル バージョンをトレースできます。

## <a name="build-automation--option-to-include-runtime-packages-in-the-deployable-package-of-the-automated-build-output"></a>ビルド自動化 - 自動ビルド出力の配置可能パッケージにランタイム パッケージを含めるオプション

ビルド定義の新しいオプションでは、自動ビルドに指示を出して、ビルド出力用に生成された配置可能なパッケージのすべてのソース管理ランタイム パッケージを含めるようにします。 これにより、お客様は、カスタム コードと ISV などのサード パーティが提供するランタイム パッケージの両方が含まれる、自動ビルドによって生成された 1 つのパッケージを展開できます。

## <a name="document-management--attachment-storage-cleanup"></a>ドキュメント管理 - ストレージ クリーンアップの添付ファイル

Dynamics AX 7.0 がリリースされたとき、添付ファイル用のデータベースの記憶領域が使用されなくなりました。ただし、移行する必要のあるプラットフォーム機能が一部残っています。 Dynamics 365 for Operations プラットフォーム更新プログラム 6 では、最後に残ったプラットフォーム使用状況が削除され、移行ボタンが**ドキュメント管理パラメーター** フォームに追加されました。 移行ボタンを使用して、アップグレード後にデータベースに残っている可能性のあるファイルをクリーンアップすることができます。 移行により、データベースに格納されている添付ファイルが BLOB ストレージに移行されます。 詳細については、[最新のプラットフォーム更新プログラムにアップグレード](../../dev-itpro/migration-upgrade/upgrade-latest-platform-update.md) を参照してください。

## <a name="number-sequence-scope-extensibility"></a>番号順序スコープの拡張性

拡張機能を通じて番号シーケンス スコープを拡張することができるようになりました。 数字シーケンスの範囲は、数字シーケンスを使用する組織を定義します。 スコープを会計年度期間と組み合わせて、さらに特定の数値シーケンスを作成することができます。 詳細については、「[番号順序スコープの拡張](../../dev-itpro/extensibility/extend-number-sequence-scope.md)」を参照してください。

## <a name="mobile"></a>携帯電話

- 異なるユーザー グループに対してワークスペースの表示を設定する機能が追加されました。

    - モバイル ユーザーに、Web クライアントで基になるフォームにアクセスできないページは表示されません。 プラットフォーム更新プログラム 6 より前に、いずれかのページにアクセスできない場合は空のモバイル ワークスペースが表示されます。 また、ユーザーのグループに対してワークスペース全体の表示を変更することができません。
    - 新しいセキュリティ属性と API が導入され、メニュー項目に基づいたモバイル ワークスペースの表示を宣言しやすくなります。 これらの API を使用して、特定のユーザー グループのモバイル ワークスペースへのアクセスを無効にできます。

- 必要な属性を自動検出する機能が追加され、フォームとテーブル メタデータを使用して、データの入力中に必須としてモバイル フィールドを示します。 アクション データは、必要なフィールドの値が指定されない場合、サーバーに送信することはできません。 (要求: プラットフォーム更新プログラム 6 とモバイルの 4 月リリース。)
- Dynamics 365 for Operations がサポートするすべての言語のモバイル ワークスペースを完全にローカライズするためのオプション。

## <a name="ideas-portal"></a>アイデア ポータル

Dynamics 365 for Operations アイデア フォーラムは、[アイデア ポータル.](https://experience.dynamics.com/ideas/) で使用可能です。 アイデア ポータルでは、すべての Dynamics 365 for Operations ユーザーは、定期的に新しいアイデアを送信、既存のアイデアを採決、およびそのアイデアの状態を追跡することができます。 これは、現在、製品の外部 ([http://experience.dynamics.com/ideas](http://experience.dynamics.com/ideas/)) およびアプリケーション内の両方から達成できます。 このスクリーンショットは、Dynamics 365 for Operations からアイデア ポータルにナビゲートする方法を示しています。

[![ideas-menu](./media/ideas-menu.png)](./media/ideas-menu.png)

Dynamics 365 for Operations フォーラムに移動するには**アイデア**のリンクをクリックします。

[![ideas-page](./media/ideas-page.png)](./media/ideas-page.png)

- フォーラムには既存のアイデアがあらかじめ設定されているため、顧客やパートナーはすぐに新しいアイデアを投票したり提案したりすることができます。
- 状態および時間を使用してアイデアをフィルター処理することができます。 上位のアイデア、話題のアイデア、および新しいアイデアを素早く表示することもできます。
- 特定のアイデアにアップ投票またはダウン投票することができます (アイデアごとに 1 票)。 新しいアイディアを投票したり提案したりするには、Microsoft アカウントを使用してサインインする必要があります。
- **個人用フィードバック** 機能を使用すると、提出された提案、提案のステータス、受け取った合計投票数の詳細なビューを表示できます。

[![ideas-options](./media/ideas-options.png)](./media/ideas-options.png)
