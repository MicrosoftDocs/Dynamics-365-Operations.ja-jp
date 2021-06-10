---
title: Dynamics 365 for Retail バージョン 10.0.5 の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Retail の新機能または変更された機能について説明します。
author: josaw1
ms.date: 09/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-08-02
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4128a3d5469eb5b9f073c8f2ba7dc47b8c13e342
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022093"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-retail-version-1005"></a>Dynamics 365 for Retail バージョン 10.0.5 の新機能および変更された機能


[!include [banner](../../includes/banner.md)]

このトピックでは、Dynamics 365 Retail 10.0.5 の新機能または変更された機能について説明します。 


Microsoft Dynamics 365 for Finance and Operations の機能については、[Finance and Operations バージョン 10.0.5 (2019 年 10 月) の新機能と変更点](/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-10-0-5) を参照してください。

## <a name="test-recorder-and-regression-suite-automation-tool-for-retail-cloud-pos"></a>Retail Cloud POS 用のレコーダーおよび Regression Auite Automation Tool のテスト
  
### <a name="test-recorder"></a>テスト レコーダー
テストレコーダーは、ユーザー受け入れテストの時間と費用を大幅に削減するために POS に追加された新機能です。 通常、ユーザー受け入れテストは Microsoft アプリケーションの更新をおこなうか、カスタム コードと構成を自分の Retail POS 生産環境に適用することが求められます。 テストレコーダーでは、POS のすべてのコントロールおよび配布された注文管理 (DOM) 要素の正確な再現性をもって、クライアントにユーザーのアクションを記録できます。 テストレコーダーは、イベントが発生した時を取得し、該当するユーザー アクションに関するすべての関連情報をリアルタイムで保存します。 テスト レコーダーは、この情報からユーザー アクションのタイプ (ボタンのクリック、値の入力、ナビゲーションなど) と、ユーザー アクションに関連するデータ (入力データの値とタイプ、フォーム コンテキスト、レコード コンテキストなど) をキャプチャできます。 (パスワード情報は記録されません)。 テストレコーダーは、録画中にメモリ内のすべてのレコーダー情報を保持し、記録の最後に出力ファイルを生成します。 この出力ファイルには、ユーザーが実行した正確なアクションを使用して、後で RSAT ツールを使用して再生するのに役立てるために十分な詳細な情報が含まれます。

> [!NOTE]
> テスト レコーダーは、Chrome ブラウザーを使用て Cloud POS のみでサポートされ、他のブラウザーやデバイスタイプのサポートは後で追加されます。

![テスト レコーダー](../dev-itpro/media/CreateTest.png)

### <a name="regression-suite-automation-tool"></a>Regression Suite Automation Tool
Regression Suite Automation Tool (RSAT) を使用すると、機能パワーユーザーは Retail POS でテストケースを実行し、テストの実行 Azure DevOps 結果をレポートおよび調査に対して再度更新できます。 RSAT には、テストの失敗を調査するためのオプションが用意されています。 RSAT では、テストパラメーターをテストステップから切り離し、Microsoft Excel でパラメーターをファイルに格納して、テストパラメーター値を簡単に編集できるようにします。 これで、RSATツールは Retail POS タブで更新され、Retail POS の記録を再生し、小売パラメーターと変数ファイルを生成するための小売固有の設定を指定します。

![POS 再生の環境設定](../dev-itpro/media/Settings.PNG)

POSとRSATの詳細については、[Retail Cloud POS 用のレコーダーおよび Regression Suite Automation Tool のテスト](../dev-itpro/pos-rsat.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2019 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2019wave2/index) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]