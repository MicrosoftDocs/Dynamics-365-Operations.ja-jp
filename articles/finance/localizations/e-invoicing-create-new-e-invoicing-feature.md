---
title: 新しい電子請求機能を作成する
description: このトピックでは、国または地域ですぐに使用できる構成可能な機能がない場合に、新しい電子請求機能を作成する方法について説明します。
author: gionoder
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffef49c78fd0564db7a2329580ad33a9ccc633c8ac74557e625d1cfb29931576
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744938"
---
# <a name="create-a-new-electronic-invoicing-feature"></a>新しい電子請求機能を作成する

[!include [banner](../includes/banner.md)]

このトピックでは、国または地域ですぐに使用できる構成可能な機能がない場合に、新しい電子請求機能を作成する方法について説明します。

新しい電子請求機能を作成するには、次のタスクを実行します :

1. 提供されている請求書モデル構成を使用し、作成する機能の既存の請求書マッピングを利用して、新しいファイル形式構成を作成します。
2. ファイル形式の構成を電子請求機能の構成に追加します。
3. 電子請求機能のセットアップを作成します。
4. 新しい電子請求機能を完成させ、組織のグローバル リポジトリに公開します。
5. 新しい電子請求機能をサービス環境にデプロイします。

## <a name="create-new-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>既存の請求書モデルから派生した新しいファイル形式の構成を作成します

この手順では、作成する新しい電子請求機能に必要なファイル形式の構成を作成します。 電子請求書ファイル形式の構成と、新しい電子請求機能で必要になる可能性のあるその他のファイル形式の構成を作成できます。

この手順を開始する前に、Regulatory Configuration Service (RCS) アカウントにサインインしてください。

1. Microsoft Dynamics 365 Finance の **電子レポート** ワークスペースで、**Microsoft** 構成プロバイダーの **リポジトリ** を選択します。
2. **グローバル** を選択し **開く** を選択して、左側のペインで **請求書モデル** の構成を選択します。

    > [!IMPORTANT]
    > ブラジルの場合は、代わりに **会計ドキュメント** モデル構成を選択します。

3. **設定** タブで **インポート** を選択します。
4. ページを閉じます。
5. ページを閉じます。
6. **レポート構成** タイルを選択してから、インポートした請求書モデルを選択します。
7. **構成の作成** を選択し、**請求書コンテキスト モデルに基づくフォーマット** を選択します。
8. フォーマット構成の名前と説明を入力します。
9. **フォーマット タイプ** フィールド、ファイル拡張子の種類を選択します。
10. **構成の作成** を選択してから、作成したフォーマット構成を選択します。
11. **デザイナー** を選択し、形式デザイナー ツールを使用して、ファイル形式の仕様を満たすようにファイル レイアウトを構成します。
12. ページを閉じます。
13. **バージョン** タブで、**ステータスの変更** \> **完了** を選択します。
14. **ステータスの変更**\>**共有** を選択して、フォーマット構成をグローバル リポジトリに公開します。

新しいファイル形式の構成は、電子請求サービスで構成を使用する前に、Microsoft ドメインと共有する必要があります。

1. 作業しているフォーマット構成を選択します。 構成のステータスは **共有** である必要があります。
2. **バージョン** タブを選択し、**高度な共有** \> **グローバル リポジトリ** を選択します。
3. **共有** タブで、**組織** を選択します。
4. **パラメーター** フィールドに、**Microsoft.com** と入力して、フォーマット構成を Microsoft ドメインと共有します。
5. **OK** を選択します。

## <a name="create-the-new-electronic-invoicing-feature"></a>新しい電子請求機能を作成する

1. RCS の **グローバリゼーション機能** ワークスペースの **機能** セクションで、**電子請求** タイルを選択します。
2. **追加** を選択してから **新機能** を選択します。
3. 電子請求機能の名前と説明を入力します。
4. **機能の作成** を選択します。

## <a name="add-electronic-invoicing-feature-configurations"></a>電子請求機能の構成を追加する

1. 作業中の電子請求機能を選択します。
2. **設定** タブで **追加** を選択します。
3. **構成** グリッドでは、電子請求書機能で電子請求書ファイルを生成するために必要なファイル形式の設定を参照して選択します。
4. **OK** を選択します。

## <a name="add-electronic-invoicing-feature-setups"></a>電子請求機能設定を追加する

1. **設定** タブで、**追加** を選択し、**カスタム設定** を選択します。
2. 機能設定の名前と説明を入力します。
3. **設定タイプ** フィールドで、**処理パイプライン** を選択します。
4. **作成** を選択します。
5. 作業中のセットアップを選択してから、**編集** を選択します。
6. **パイプラインの処理** タブで、**新規** を選択してパイプライン アクションを追加します。 パイプラインの詳細については、[アクション](e-invoicing-configuration-rcs.md#actions)を参照してください。
7. **適用ルール** タブで、**新規作成** を選択し、適用ルール条項を追加します。 適用ルールの詳細については、[適用ルール](e-invoicing-configuration-rcs.md#applicability-rules)を参照してください。
8. **変数** タブで、**新規作成** を選択して必要に応じて変数を追加します。
9. **保存** を選択し、**検証** を選択して構成の整合性を確認します。
10. ページを閉じます。

## <a name="deploy-the-electronic-invoicing-feature-to-the-service-environment"></a>電子請求機能をサービス環境にデプロイします

このタスクを完了する方法については、[電子請求機能をサービス環境にデプロイする](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment)を参照してください。

## <a name="deploy-the-electronic-invoicing-feature-to-a-connected-application"></a>接続されたアプリケーションに電子請求機能をデプロイする

このタスクを完了する方法については、[アプリケーションセットアップの構成](e-invoicing-get-started.md#configure-the-application-setup)および[接続されたアプリケーションへの電子請求機能の展開](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application)を参照してください。
