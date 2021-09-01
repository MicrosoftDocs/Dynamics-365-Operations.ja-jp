---
title: 電子申告 (ER) コンフィギュレーションのインポート
description: このトピックでは、Lifecycle Services (LCS) からローカルのビジネス データ アプリケーションに電子申告 (ER) の構成をインポートする方法について説明します。
author: NickSelin
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport
audience: Developer
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.openlocfilehash: fd28d513ee79d26192b768308ace8525ce271c0229733f1a7105a1cebb1390f7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772046"
---
# <a name="import-electronic-reporting-er-configurations"></a>電子申告 (ER) コンフィギュレーションのインポート

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) からローカルのビジネス データ アプリケーションに[電子申告 (ER) のコンフィギュレーション](general-electronic-reporting.md#Configuration) をダウンロードする方法について説明します。 また、ER リポジトリからローカル ビジネス データ (LBD) アプリケーションに ER 構成をアップロードする方法についても説明します。

> [!IMPORTANT]
> ER コンフィギュレーションの記憶域リポジトリとして LCS を使用することは[廃止される](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release) 予定です。 詳細については、[Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 記憶域の廃止](../../../finance/localizations/rcs-lcs-repo-dep-faq.md) を参照してください。

1. 次のロールのいずれかを使用して、ローカル ビジネス データ アプリケーションにログインします。

    * 電子申告開発者
    * 電子申告機能コンサルタント
    * システム管理者

2. **組織管理** \> **電子申告** の順に移動します。
3. **コンフィギュレーション プロバイダー** セクションで、会社に関連付けられている ER プロバイダーのカードを選択します。

    > [!NOTE]
    > 新しい ER ソリューション プロバイダを登録する方法については、**構成プロバイダーを作成し、アクティブとしてマークする<** タスク ガイドを再生してください。

4. 選択したタイルで、**リポジトリ** をクリックします。


5. **コンフィギュレーション リポジトリ** ページのグリッドで、**ファイル システム** タイプの既存のリポジトリを選択します。 このリポジトリがグリッドに表示されない場合は、次の手順に従います。

    1. **追加** をクリックして新しいリポジトリを追加します。
    2. リポジトリ タイプとして、**FILE SYSTEM** を選択します。
    3. **リポジトリの作成** をクリックします。
    4. リポジトリの名前と説明を入力します。
    5. レポジトリの作業ディレクトリのパスを入力します。 このパスは、リポジトリに属する ER 構成が格納されるローカル ファイル システムのフォルダーを指している必要があります。
    6. **OK** をクリックして、新しいリポジトリを確認および保存します。
    7. グリッドで、**ファイル システム** タイプの新しいリポジトリを選択します。

6. ブラウザーで、別のタブを開き、LCS にサインインします。
7. 共有アセット ライブラリで、**GER コンフィギュレーション** アセット タイプを選択してから **すべてダウンロード** をクリックします。

    > [!NOTE]
    > すべての ER コンフィギュレーションはダウンロードのため ZIP ファイルに入れられます。

8. ファイルを開いて、すべての ER コンフィギュレーションを選択し、**ファイル システム** タイプのリポジトリの作業ディレクトリにコピーします。
9. **ER リポジトリ** ページの、**Dynamics 365 for Finance and Operations** タブで、**開く** をクリックして、選択されたリポジトリの ER コンフィギュレーションの一覧を表示します。
10. 左ウィンドウの **コンフィギュレーション** ツリーで、ER コンフィギュレーションを選択します。
11. **バージョン** クイック タブで、ER コンフィギュレーションの必要なバージョンを選択します。
12. **インポート** をクリックして、このリポジトリから現在のインスタンスに選択したバージョンをダウンロードします。

    > [!NOTE]
    > **インポート** ボタンは、既存の ER コンフィギュレーション バージョンには使用できません。

> [!NOTE]
> ER の設定に応じて、コンフィギュレーションはインポートされた後に検証されます。 不整合または問題が検出されると、通知を受け取る場合があります。 インポートしたコンフィギュレーションのバージョンを使用する前に、こうした不整合や問題を解決する必要があります。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**質問:** 共有アセット ライブラリで **すべてダウンロード** をクリックすると、次の警告が表示されます: Zip の生成が進行中です。数分後にもう一度お試しください。 なぜこの警告を受信するのですか。

**回答:** これは、新しいコンフィギュレーションが共有アセット ライブラリに追加され、ER コンフィギュレーションがアーカイブされているため、この警告が表示されます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
