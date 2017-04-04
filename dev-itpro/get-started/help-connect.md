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

このトピックでは、のMicrosoft Dynamics 365のヘルプ システムのコンポーネントについて説明します。 これは方法の概要を方法でこれらのコンポーネントおよび集計を関連付けるカスタム ヘルプを作成する方法を説明します。 

<a name="help-architecture"></a>ヘルプ アーキテクチャ
-----------------

次の図は、工程のヘルプ システム365 for Operationsの一部を示します。 製品のヘルプ システムはhttps://docs.microsoft.comの工程のサイト365 for Operationsの記事を引っ張ります、タスクは、Lifecycle Services (LCS)に業務プロセスのModelerに格納されて説明します。 
**注記: **アスタリスク (\*) を含むダイアグラムに表示される機能が計画されますが、まだ使用できません。 [![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>ヘルプ システムの接続
**システム パラメータ**ページを使用して、システム管理者が実装用のヘルプ システムの品目を関連付けます。 [![システム![設定では、ヘルプ"] (。/media/system-parameters_ops-1024x437.png) ] (。**システム パラメータ**ページでは、/media/system-parameters_ops.png、次の手順に従います。:

1.  **重要: **最初に、Lifecycle Servicesに**ヘルプ**タブ、関連付ける必要があります開きます。 フォームの途中でリンクをクリックするしてくださいい接続、決算のダイアログ ボックス待ち、[**システム パラメータ**ページに取得するために**良い**クリックします。[。[LCSに関連付けます。] (。/media/connectにlcs穀物は、「」1024x365.png LCSに接続します) ] (。/media/connectにlcscrop.png) 
2.  接続する Lifecycle Services プロジェクトを選択します。
3.  タスク記録を取得する BPM ライブラリ (選択したプロジェクト内) を選択します。
4.  BPM ライブラリの表示順序を選択します。 これにより、ライブラリからのタスク記録が [**ヘルプ**] ウィンドウに表示される順序が決まります。

これらの手順を完了したら、[**ヘルプ**] ウィンドウを開いて [**タスク ガイド** タブをクリックします。 これで、Dynamics 365 for Operations の現在のページに対応するタスク ガイドを表示できます。 タスク ガイドがない場合は、検索するキーワードを入力できます。

### <a name="showing-translated-task-guides"></a>翻訳されたタスク ガイドの表示

変換されたタスク ガイドは5年1月2016日のAPQCで統一されたライブラリと終了のライブラリに最初に出荷されました。 Microsoft Dynamics 365 for Operations でローカライズされたタスク ガイドのヘルプを参照するには、5 月のライブラリに接続できることを確認してください。 このガイドは、な言語は**オプション** **ユーザー設定での言語設定で、ユーザーに &gt; 対してアクセスを制御します。**。 **注記:** 多くの作業ガイドが翻訳されていますが、現在 Dynamics 365 for Operations クライアントには翻訳済みのタスク ガイド名は表示されません。 また、2年1月2016日にリリースされたタスクについてのみ5年のライブラリの変換に使用できます。 翻訳の追加のあるライブラリ更新をリリース予定です。

-   タスク ガイドが翻訳されている場合、そのタスク ガイドを開くと、タスク ガイドのすべてのテキストは選択した言語で表示されます。
-   タスク ガイドが翻訳されていない場合、それを開くと、一部のテキスト (コントロールのテキスト) のみが選択した言語で表示されます。

## <a name="creating-custom-help"></a>カスタム ヘルプの作成
実装を反映するタスク記録を作成して LCS 業務プロセス ライブラリに保存することで、Dynamics 365 for Operations の実装へ向けてカスタム ヘルプを作成できます。 パートナーの場合、ライブラリを会社のライブラリに昇格してソリューションに含める場合、顧客が使用できます。 APQC 統合グローバル ライブラリのコピーを作成して開き、タスクの記録を開いて変更し、変更がある記録を保存します。 詳細については、" [タスク記録をドキュメントやトレーニングとして使用する作成する方法] (。/user-interface/task-recorder.md)。

<a name="see-also"></a>参照
--------

[Help overview](help-overview.md)

[タスク レコーダの概要] (。/user-interface/task-recorder.md) 

[ドキュメントやトレーニングとして使用するタスク記録の作成方法](../user-interface/task-recorder-training-docs.md)

[Lifecycle Servicesで、Dynamics 365 for Operationsの[トレーニングのライブラリのタスク レコーダ (外部リンクを使用して作成します) ] (https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)


