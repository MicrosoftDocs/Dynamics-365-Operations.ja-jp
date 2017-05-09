---
title: "ヘルプ システムに接続する"
description: "このトピックでは、Microsoft Dynamics 365 for Operations のヘルプ システムのコンポーネンツについて説明し、それらを関連付ける方法の概要や、独自のヘルプを作成する方法について説明します。"
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5ac5e30cff2239f601778001368fa7aaba478f5c
ms.lasthandoff: 03/31/2017


---

# <a name="connect-the-help-system"></a>ヘルプ システムに接続する

このトピックでは、Microsoft Dynamics 365 for Operations のヘルプ システムのコンポーネントについて説明します。 これらのコンポーネントを関連付ける方法の概要や、独自のヘルプを作成する方法について説明します。 

<a name="help-architecture"></a>ヘルプ アーキテクチャ
-----------------

次の図では、Microsoft Dynamics 365 for Operations のヘルプ システムの一部を示します。 製品内ヘルプ システムは https://docs.microsoft.com の Dynamics 365 for Operations サイト、Lifecycle Services (LCS) のビジネス プロセス モデラーに格納されているタスク ガイドから記事を参照します。 
**注記:** 図にアスタリスク (\*) 付きで表示される機能は計画されているもので、まだ使用できません。 [![ヘルプ アーキテクチャ](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>ヘルプ システムの接続
**システム パラメーター** ページを使用して、システム管理者は実装に向けてヘルプ システムのピースを繋ぎ合せます。 [![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) **システム パラメーター** ページで次の手順に従います。

1.  **重要:** [**ヘルプ**] タブを初めて開く際には、Lifecycle Services に接続する必要があります。 フォームの中程のリンクをクリックし、接続されるまで待機し、ダイアログ ボックスを閉じ、[**OK**] をクリックして**システム パラメーター** ページを取得します。[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)
2.  接続する Lifecycle Services プロジェクトを選択します。
3.  タスク記録を取得する BPM ライブラリ (選択したプロジェクト内) を選択します。
4.  BPM ライブラリの表示順序を選択します。 これにより、ライブラリからのタスク記録が [**ヘルプ**] ウィンドウに表示される順序が決まります。

これらの手順を完了したら、[**ヘルプ**] ウィンドウを開いて [**タスク ガイド** タブをクリックします。 これで、Dynamics 365 for Operations の現在のページに対応するタスク ガイドを表示できます。 タスク ガイドがない場合は、検索するキーワードを入力できます。

### <a name="showing-translated-task-guides"></a>翻訳されたタスク ガイドの表示

翻訳されたタスク ガイドは、2016 年 5 月の APQC 統合ライブラリおよび「はじめに」ライブラリで初めて同梱されました。 Microsoft Dynamics 365 for Operations でローカライズされたタスク ガイドのヘルプを参照するには、5 月のライブラリに接続できることを確認してください。 タスク ガイドの表示言語は、[**オプション**] &gt; [**基本設定**] の [言語の設定] でユーザーごとに制御されます。 **注記:** 多くの作業ガイドが翻訳されていますが、現在 Dynamics 365 for Operations クライアントには翻訳済みのタスク ガイド名は表示されません。 また、現時点では 2016 年 2 月にリリースされたタスク ガイドのみが 5 月のライブラリで翻訳版として利用可能です。 翻訳の追加のあるライブラリ更新をリリース予定です。

-   タスク ガイドが翻訳されている場合、そのタスク ガイドを開くと、タスク ガイドのすべてのテキストは選択した言語で表示されます。
-   タスク ガイドが翻訳されていない場合、それを開くと、一部のテキスト (コントロールのテキスト) のみが選択した言語で表示されます。

## <a name="creating-custom-help"></a>カスタム ヘルプの作成
実装を反映するタスク記録を作成して LCS 業務プロセス ライブラリに保存することで、Dynamics 365 for Operations の実装へ向けてカスタム ヘルプを作成できます。 パートナーの場合、ライブラリを会社のライブラリに昇格してソリューションに含める場合、顧客が使用できます。 APQC 統合グローバル ライブラリのコピーを作成して開き、タスクの記録を開いて変更し、変更がある記録を保存します。 詳細については、「[How to create a task recording to use as documentation or training](../user-interface/task-recorder.md)」を参照してください。

<a name="see-also"></a>参照
--------

[ヘルプ概要](help-overview.md)

[タスク レコーダーの概要](../user-interface/task-recorder.md)

[ドキュメントやトレーニングとして使用するタスク記録の作成方法](../user-interface/task-recorder-training-docs.md)

[タスク レコーダー (外部リンク) を使用してライフ サイクル サービス内での Dynamics 365 for Operations のトレーニングの新しいライブラリを作成](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)


