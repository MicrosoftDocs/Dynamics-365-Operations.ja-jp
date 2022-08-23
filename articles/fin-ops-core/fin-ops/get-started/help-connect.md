---
title: 財務と運用アプリのヘルプ エクスペリエンスの構成
description: この記事では、一部の Microsoft Dynamics 365 アプリのヘルプシステムのコンポーネントに関する情報を提供します。
author: edupont04
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: edupont
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.form: SystemParameters
ms.openlocfilehash: 35dc37f6669a3f47dd82917be0e84d0b8698e8f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282468"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>財務と運用アプリのヘルプ エクスペリエンスの構成

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

この記事では、Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce、および Dynamics 365 Human Resources などの財務と運用アプリに関するヘルプ システムのコンポーネントの概要を説明します。 また、この記事では、これらのコンポーネントの接続方法と、ユーザー定義のヘルプを作成するプロセスの概要についても説明します。

## <a name="help-architecture"></a>ヘルプ アーキテクチャ

財務と運用アプリには、[Microsoft Dynamics 365 ドキュメント](/dynamics365/) サイトにて公開されている概要やその他のトピックが含まれています。 このコンテンツには、製品内の **ヘルプ** ウィンドウからアクセスできます。 次の図は、ヘルプ システムの一部を示します。

[![ヘルプ アーキテクチャ。](./media/help-architecture.png)](./media/help-architecture.png)

製品内のヘルプ システムでは、docs.microsoft.com やその他の接続 web サイトから記事を取得しています。 また、Microsoft Dynamics Lifecycle Services (LCS) 内の業務プロセス (BPM) にて保管されているタスクガイドも取得しています。

## <a name="adding-task-guides"></a>タスク ガイドの追加

> [!NOTE]
> 現時点では、**タスク ガイド** タブは人事管理やコマースでは使用できません。 <!--We are currently working to enable this functionality in a future release.--> しかし、人事管理内の [はじめに] のタスク ガイドは、基本機能の一環として利用可能となっています。 コマースおよび人事管理のの手順ガイドは、[Microsoft Dynamics 365 ドキュメント](/dynamics365/) サイトで利用可能です。

**システム パラメーター** ページでは、システム管理者は、実装に関連するタスク ガイド ライブラリへのアクセスを構成できます。

> [!NOTE]
> - ヘルプを構成するには、アプリを導入しているテナントと同じアカウントを使用してサイン インする必要があります。
> - ローカル仮想ハード ドライブ (VHD) で実行されているアプリのインスタンスからは、LCS ライブラリに接続することはできません。

[![システム パラメーター フォームとヘルプ設定。](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

ソリューションの作業ガイドを構成するには、**システム パラメーター** のページで次の手順を実行 します。

> [!IMPORTANT]
> 初めて **ヘルプ** タブを開く際には、Lifecycle Services に接続する必要があります。 フォームの中程のリンクを選択し、接続されるまで待機します。ダイアログ ボックスを閉じ、**OK** を選択して **システム パラメーター** ページを取得します。
>
> [![LCS に接続](./media/connect-to-lcs-crop-1024x365.png "LCS に接続します。")](./media/connect-to-lcs-crop.png)

1. 接続する Lifecycle Services プロジェクトを選択します。
2. タスク記録を取得する BPM ライブラリ (選択したプロジェクト内) を選択します。
3. BPM ライブラリの表示順序を選択します。 表示順序では、ライブラリからのタスク録画が **ヘルプ** ウィンドウに表示される順序を定義します。

これらのステップを完了したのちに、**ヘルプ** ウィンドウを開いて **タスク ガイド** タブを選択できます。財務と運用アプリケーションの現在のページに対応するタスク ガイドが表示されるようになります。 タスク ガイドがない場合は、検索するキーワードを入力できます。

### <a name="showing-translated-task-guides"></a>翻訳されたタスク ガイドの表示

翻訳されたタスク ガイドは、2016 年 5 月の APQC 統合ライブラリと [はじめに] ライブラリで初めて公開されました。 ローカライズされたタスク ガイドのヘルプを参照するには、ご利用の Dynamics 365 ソリューションが 2016年5月のライブラリに接続できている必要があります。 タスク ガイドの表示言語は、**オプション** &gt; **基本設定** の言語の設定で変更することができます。

> [!NOTE]
> 現在多くのタスク ガイドが翻訳されていますが、クライアントには翻訳済みのタスク ガイドの名前は表示されません。 また、2016 年 5 月のライブラリでは、2016 年 2 月に公開されたタスク ガイドの翻訳版のみが利用可能です。 Microsoft は、追加された翻訳を含む更新されたライブラリをリリース予定です。
>
> - タスク ガイドが翻訳されている場合、そのタスク ガイドを開くと、タスク ガイドのすべてのテキストは選択した言語で表示されます。
> - タスク ガイドが翻訳されていない場合、それを開くと、一部のテキスト (コントロールのテキスト) のみが選択した言語で表示されます。

## <a name="adding-custom-help"></a>ユーザー定義のヘルプを追加する

タスク ガイドを使用して、ユーザー定義のヘルプの作成や、**ヘルプ** ウィンドウにユーザー定義の web サイトを接続することができます。

### <a name="create-custom-help-by-using-task-guides"></a>タスク ガイドを使用したユーザー定義のヘルプを作成する

実装を反映したタスクの記録を作成し、LCS のビジネス プロセス ライブラリに保存することで、対応するアプリのユーザー定義のヘルプを作成することができます。 人事管理ではユーザー定義のタスク ガイドを作成することはできません。

パートナーの場合は、ライブラリを会社のライブラリに昇格してソリューションに含めることで顧客が使用することができます。 APQC 統合グローバル ライブラリのコピーを作成して開き、タスクの記録を開いて編集し、変更を保存します。 詳細については、[タスク レコーダーのリソース](../../dev-itpro/user-interface/task-recorder.md) を参照してください。

### <a name="connect-a-custom-help-site"></a>ユーザー定義のヘルプ サイトに接続する

財務と運用アプリが既成のフォームで使用されることはほとんどありません。 その代わりに、ソリューションは組織のニーズに合わせてカスタマイズされ、拡張されます。 また、ヘルプ エクスペリエンスをカスタマイズ、拡張することが可能です。 たとえば、製品内の **ヘルプ** ウィンドウにユーザー定義のヘルプを追加できます。

Microsoft では、ユーザー定義のヘルプを展開して **ヘルプ** ウィンドウに接続するツールキットを提供しています。 **ヘルプ** ウィンドウに接続されているユーザー定義のヘルプ ソリューションを設定する方法の詳細については 、[カスタムヘルプの概要](../../dev-itpro/help/custom-help-overview.md)を参照してください。

ヘルプをカスタマイズするのツールやプロセスを Microsoft と連携したい場合は、[https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback) のフォームに記入してください。

## <a name="see-also"></a>参照

[ヘルプ システム](help-overview.md)  
[カスタム ヘルプの概要](../../dev-itpro/help/custom-help-overview.md)  
[タスク レコーダー リソース](../../dev-itpro/user-interface/task-recorder.md)  
[タスク レコーダーを使用したドキュメントやトレーニングの作成](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[カスタム ヘルプ GitHub リポジトリ](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

