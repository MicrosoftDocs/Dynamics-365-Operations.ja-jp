---
title: グローバリゼーション機能を完了、公開、配置する
description: この記事では、グローバリゼーション機能のライフサイクルに関する情報について説明します。
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 9d4a408f2169b220fefd9ab7e9f3b37217fb3cfe
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710838"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>グローバリゼーション機能を完了、公開、配置する

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>電子請求機能のバージョン

電子請求機能の機能はバージョン管理されています。 新しいバージョンを作成すると、バージョン番号が自動的に増番で付与されます。

電子請求機能のバージョンは、最大で 3 つのステータスを持つライフサイクルに従います。

- **下書き** – 機能バージョンがこの状態にある場合、構成の属性とそのコンポーネント (ファイル形式の構成など) を編集できます。
- **完了** – この状態は、機能バージョンの編集が完了し、これ以上更新を行わない場合に表示されます。 機能バージョンの状態が「完了」の場合は、機能バージョンまたはそのコンポーネントの編集はできなくなります。
- **公開済み** – この状態は、機能のバージョンが組織に関連付けられているグローバル リポジトリに公開されていることを表わします。 機能バージョンの状態が「完了」の場合は、機能バージョンまたはそのコンポーネントの編集はできなくなります。

電子請求機能の新しいバージョンの **有効開始** 日を指定できます。 これにより、使用できる既定のバージョンを定義したり、機能をサービス環境に配置するときに上書きすることができます。

電子請求機能のバージョンの状態を変更するには、次の手順に従います。

1. 規制構成サービス (RCS) のアカウントにログインします。
2. **グローバリゼーション機能** ワークスペースの **機能** セクションで、 **電子請求** タイルを選択します。
3. **電子請求機能** ページの左側で、電子請求機能を選択します。
4. ページの右側にある **バージョン** タブで、バージョンを選択します。
5. **状態の変更** を選択し、**完了** (状態が **ドラフト** の場合) を選択するか **公開済み** (現在の状態が **完了** の場合) を選択します。
6. 確認のメッセージ ボックスで、**はい** を選択して要求を確認します。

**完了** 状態から **公開済み** 状態の手動での変更はオプションです。 電子請求機能のバージョンは、サービス環境に配置すると **公開済み** 状態に自動的に更新されます。

状態は、**バージョン** タブの **機能バージョンの状態** 列で追跡できます。

## <a name="deploy-feature-versions"></a>機能のバージョンの展開

RCS では、**展開** コマンドを使用して電子請求機能のバージョンをターゲットのサービス環境または接続されているアプリケーションに公開します。

1. **電子請求機能** ページの左側で、電子請求機能を選択します。
2. ページの右側にある **バージョン** タブで、サービス環境または接続されたアプリケーションに展開する電子請求機能のバージョンを選択します。 選択したバージョンの状態は **完了** または **公開済み** である必要があります。
3. **展開** を選択し、次のいずれかまたは両方のオプションを選択して、展開するターゲットを定義します。

    - **接続されているアプリケーション** – これはオプションですが、アプリケーション設定によって提供される構成が、以前に関連付けられた Microsoft Dynamics 365 Finance または Dynamics 365 Supply Chain Management のインスタンスで書かれる場合は使用する必要があります。 このタイプの配置をスキップするには、財務または Supply Chain Management のアプリケーション設定で定義されたパラメータを手動でコンフィギュレーションする必要があります。
    - **サービス環境** – これは電子請求機能のバージョンがサービス環境に展開されます。 これにより、電子請求で Finance または Supply Chain Management が送信する電子ドキュメントを受信して処理することができます。

> [!NOTE]
> 通常、サービス環境に展開する必要がある電子レポート (ER) 機能のパラメータを変更します。 接続されているアプリケーションに対する変更はまれです。 アプリケーションの対応するパラメータを変更する場合にのみ、新しいバージョンを接続されているアプリケーションに展開する必要があります。

特定のバージョンの電子請求機能を特定の環境に展開するかどうかを決定するには、**環境** タブにある情報を確認します。

## <a name="remove-feature-versions"></a>機能のバージョンを削除する

RCS では、**キャンセル** を選択して、サービス環境から特定の電子請求機能のバージョンを削除します (サービス環境に展開された場合)。

> [!IMPORTANT]
> **キャンセル** ボタンはサービス環境にのみ使用できます。 現在の電子請求機能の接続されたアプリケーションからは、何も削除されません。

## <a name="rebase-electronic-invoicing-features"></a>電子請求書発行機能をリベースする

電子請求機能が別の機能から派生したものである場合、**リベース** を選択して、この派生した機能を元の機能 (親) に導入された変更を基に更新します。

作成した機能の派生バージョンをリベースするには、次の手順に従います。

1. 機能の最新バージョンをグローバル リポジトリからインポートして取得します。 詳細については、[グローバル リポジトリから機能をインポートする](e-invoicing-import-feature-global-repository.md) を参照してください。
2. 機能の一覧で、リベースする機能を選択します。
3. **バージョン** タブで、**新規** を選択して、下書きバージョンを作成します。
4. **リベース** を選択します。
5. **リベース** ダイアログ ボックスで、リベース先となる機能のバージョンを選択します。
6.  **OK** を選択します。
7. 機能コンポーネントを確認し、必要な変更を行います。
8. リベースされた機能を完了するには、**ステータスの変更** を選択します。 リベースが完了したら、追加のアクションを実行できます。

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>電子請求機能の特定のバージョンを入手する

電子請求機能の新しいバージョンを作成すると、最新の機能バージョンのコピーが作成されます。 新しいバージョンの基準として以前のバージョンの機能を使用するには、バージョンを選択し **このバージョンのコマンドを取得する** を選択します。 機能の新しいドラフト バージョンが作成され、選択したバージョンのコピーとして使用できます。
