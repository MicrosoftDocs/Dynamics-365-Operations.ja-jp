---
title: Dynamics 365 for Retail バージョン 10.0.5 の機能をプレビューする
description: このトピックでは Dynamics 365 for Retail のプレビュー中の機能について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-08-02
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 99227b40d368c7cd278608253b543f8a05dffac9
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863646"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-retail-version-1005"></a>Dynamics 365 for Retail バージョン 10.0.5 の新機能および変更された機能

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Retail 10.0.5 の新機能または変更された機能について説明します。 

Microsoft Dynamics 365 for Finance and Operations の機能の詳細については、 [Finance and Operations バージョン 10.0.5 (2019 年 10 月) の機能のプレビュー](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-10-0-5). を参照してください。

## <a name="test-recorder-and-regression-suite-automation-tool-for-retail-cloud-pos"></a>Retail Cloud POS 用のレコーダーおよRegression Suite Automation Tool のテスト
  
### <a name="test-recorder"></a>テスト レコーダー
テストレコーダーは、ユーザー受け入れテストの時間と費用を大幅に削減するために POS に追加された新機能です。 通常、ユーザー受け入れテストは Microsoft アプリケーションの更新をおこなうか、カスタム コードと構成を自分の Retail POS 生産環境に適用することが求められます。 テストレコーダーでは、POS のすべてのコントロールおよび配布された注文管理 (DOM) 要素の正確な再現性をもって、クライアントにユーザーのアクションを記録できます。 テストレコーダーは、イベントが発生した時を取得し、該当するユーザー アクションに関するすべての関連情報をリアルタイムで保存します。 テスト レコーダーは、この情報からユーザー アクションのタイプ (ボタンのクリック、値の入力、ナビゲーションなど) と、ユーザー アクションに関連するデータ (入力データの値とタイプ、フォーム コンテキスト、レコード コンテキストなど) をキャプチャできます。 (パスワード情報は記録されません)。 テストレコーダーは、録画中にメモリ内のすべてのレコーダー情報を保持し、記録の最後に出力ファイルを生成します。 この出力ファイルには、ユーザーが実行した正確なアクションを使用して、後で RSAT ツールを使用して再生するのに役立てるために十分な詳細な情報が含まれます。

> [!NOTE]
> テスト レコーダーは、Chrome ブラウザーを使用て Cloud POS のみでサポートされ、他のブラウザーやデバイスタイプのサポートは後で追加されます。

[![テスト レコーダー](.././media/CreateTest.png)](.././media/CreateTest.png)

### <a name="regression-suite-automation-tool"></a>Regression Suite Automation Tool
Regression Suite Automation Tool (RSAT) を使用すると、機能パワーユーザーは Retail POS でテストケースを実行し、テストの実行 Azure DevOps 結果をレポートおよび調査に対して再度更新できます。 RSAT には、テストの失敗を調査するためのオプションが用意されています。 RSAT では、テストパラメーターをテストステップから切り離し、Microsoft Excel でパラメーターをファイルに格納して、テストパラメーター値を簡単に編集できるようにします。 これで、RSATツールは Retail POS タブで更新され、Retail POS の記録を再生し、小売パラメーターと変数ファイルを生成するための小売固有の設定を指定します。

[![POS 再生環境設定](.././media/Setting.png)](.././media/Setting.png)

## <a name="additional-resources"></a>追加リソース

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2019 リリース ウェーブ 2 プラン](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/index) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。
