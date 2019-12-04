---
title: ヘルプ システムに接続する
description: このトピックでは、Finance and Operations アプリのヘルプ システムのコンポーネントについて説明し、それらを関連付ける方法の概要や、独自のヘルプを作成する方法について説明します。
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2955464aa8a220563db1b9ebbb348be52f520659
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812583"
---
# <a name="connect-the-help-system"></a>ヘルプ システムに接続する

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリ向けのヘルプ システムのコンポーネント (Dynamics 365 Finance、Supply Chain Management、小売業、人材など) について説明します。 これらのコンポーネントを関連付ける方法の概要や、独自のヘルプを作成する方法について説明します。

## <a name="help-architecture"></a>ヘルプ アーキテクチャ

次の図は、ヘルプ システムの一部を示します。 製品内ヘルプ システムは https://docs.microsoft.com、Lifecycle Services (LCS) のビジネス プロセス モデラーに格納されているタスク ガイドから記事を参照します。

> [!NOTE]
> 図にアスタリスク (\*) 付きで表示される機能は計画されているもので、まだ使用できません。

[![ヘルプ アーキテクチャ](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>ヘルプ システムの接続

> [!NOTE]
> **タスク ガイド** タブは、現在 Dynamics 365 Talent および Retail では使用できません。 将来のリリースではこの機能を有効にするよう、作業が進行中です。 [Talent] での [はじめに] の経験タスク ガイドは、基本的機能をカバーするために引き続き使用可能です。 Retail および Talent の両方に関する docs.microsoft.com サイト上でも利用可能な、手順を追ったヘルプ。

**システム パラメーター** ページを使用して、システム管理者は実装に向けてヘルプ システムのピースを繋ぎ合せます。

[![システム パラメーター フォームとヘルプ設定](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

**システム パラメーター** ページで、次の手順に従います。

> [!IMPORTANT]
> 初めて **ヘルプ** タブを開く際には、Lifecycle Services に接続する必要があります。 フォームの中程のリンクをクリックし、接続されるまで待機し、ダイアログ ボックスを閉じ、**OK** をクリックして**システム パラメーター**ページを取得します。
>
> [![LCS に接続](./media/connect-to-lcs-crop-1024x365.png "LCS に接続")](./media/connect-to-lcs-crop.png)

1. 接続する Lifecycle Services プロジェクトを選択します。
2. タスク記録を取得する BPM ライブラリ (選択したプロジェクト内) を選択します。
3. BPM ライブラリの表示順序を選択します。 これにより、ライブラリからのタスク記録が **ヘルプ** ウィンドウに表示される順序が決まります。

これらのステップを完了したのちに、**ヘルプ** ウィンドウを開いて**タスク ガイド** タブをクリックできます。Finance and Operations アプリケーションの現在のページに対応するタスク ガイドが表示されるようになります。 タスク ガイドがない場合は、検索するキーワードを入力できます。

### <a name="showing-translated-task-guides"></a>翻訳されたタスク ガイドの表示

翻訳されたタスク ガイドは、2016 年 5 月の APQC 統合ライブラリおよび「はじめに」ライブラリで初めて同梱されました。 Finance and Operations アプリケーションでローカライズされたタスク ガイドのヘルプを参照するには、5 月のライブラリに接続できることを確認してください。 タスク ガイドの表示言語は、**オプション** &gt; **基本設定** の [言語の設定] でユーザーごとに制御されます。

> [!NOTE]
> 多くの作業ガイドが翻訳されていますが、現在クライアントには翻訳済みのタスクガイドの名前は表示されません。 また、現時点では 2016 年 2 月にリリースされたタスク ガイドのみが 5 月のライブラリで翻訳版として利用可能です。 翻訳の追加のあるライブラリ更新をリリース予定です。
>
> - タスク ガイドが翻訳されている場合、そのタスク ガイドを開くと、タスク ガイドのすべてのテキストは選択した言語で表示されます。
> - タスク ガイドが翻訳されていない場合、それを開くと、一部のテキスト (コントロールのテキスト) のみが選択した言語で表示されます。

## <a name="creating-custom-help"></a>カスタム ヘルプの作成

タスク ガイドを使用して、カスタム ヘルプを作成したり、ヘルプ ウィンドウを Web サイトに接続できます。

### <a name="create-custom-help-with-task-guides"></a>タスク ガイドを使用したカスタム ヘルプの作成

実装を反映するタスク記録を作成して LCS 業務プロセス ライブラリに保存することで、財務、Supply Chain Management、および小売のカスタム ヘルプを作成できます。 [Talent] のカスタム タスク ガイドを作成することはできません。

パートナーの場合、ライブラリを会社のライブラリに昇格してソリューションに含める場合、顧客が使用できます。 APQC 統合グローバル ライブラリのコピーを作成して開き、タスクの記録を開いて変更し、変更がある記録を保存します。 詳細については、[タスク レコーダーのリソース](../../dev-itpro/user-interface/task-recorder.md) を参照してください。

### <a name="connect-a-custom-site"></a>カスタム サイトを接続する

Microsoft は、カスタム ヘルプのサイトを作成およびヘルプ ウィンドウに接続する方法について説明するホワイト ペーパーおよびサンプル コードを提供しています。 詳細については、以下を参照してください。

- [Finance and Operations アプリケーションのカスタム ヘルプの作成 (ホワイト ペーパー)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [カスタム ヘルプ GitHub リポジトリ](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>追加リソース

[ヘルプ システム](help-overview.md)

[タスク レコーダー リソース](../../dev-itpro/user-interface/task-recorder.md)

[タスク レコーダーを使用したドキュメントやトレーニングの作成](../../dev-itpro/user-interface/task-recorder-training-docs.md)
