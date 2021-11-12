---
title: 税コンフィギュレーションにデータ フィールドを追加する
description: このトピックでは、データ フィールドを追加して税コンフィギュレーションをカスタマイズする方法について説明します。
author: Kai-Cloud
ms.date: 10/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 590c2d62995f260ba4277e1031349b0dc43f1417
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674903"
---
# <a name="add-data-fields-in-tax-configurations"></a>税コンフィギュレーションにデータ フィールドを追加する

[!include [banner](../includes/banner.md)]

このトピックでは、[税統合で追加されたデータ フィールド](tax-service-add-data-fields-tax-integration-by-extension.md)を使用して、税コンフィギュレーション をカスタマイズする方法について説明します。

## <a name="customize-the-tax-data-model"></a>税データ モデルをカスタマイズする

1. Microsoft Dynamics 365 Finance で、**電子申告** > **税の構成** の順に移動します。
2. コンフィギュレーション ツリーで、**税計算データ モデル** を選択します。 次に、アクション ウィンドウで、**構成の作成** を選択します。 

  > [!NOTE] 
  > 使用できるコンフィギュレーション プロバイダーが 1 つもいない場合は、それを作成して、税コンフィギュレーションに対して有効にします。 詳細については、[構成プロバイダーを作成して、有効としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。
  
3. ドロップダウン ダイアログ ボックスで、**名前から派生した課税対象ドキュメント モデル: 税計算データ モデル、Microsoft** を選択し、新しい税データ モデルの名前を入力し、**コンフィギュレーションの作成** を選択します。
4. 作成した税データ モデルを選択し、アクション ウィンドウで **デザイナー** を選択します。
5. データ モデル ツリーを展開し、**明細行** を 選択して、**新規** を選択します。
6. **ノードの作成** ダイアログ ボックスに名前を入力し、アイテムの種類を指定して、**追加** を選択します。
7. 必要な列を追加します。
8. アクション ウィンドウで、**保存** を選択してから、**完了** を選択します。
9. ページを閉じて、完成したバージョンの税データ モデルを表示します。

## <a name="customize-the-tax-configuration"></a>税コンフィギュレーションをカスタマイズする

1. Finance で、**電子申告** > **税の構成**.の順に移動します。
2. コンフィギュレーション ツリーで、**税計算コンフィギュレーション** を選択します。 次に、アクション ウィンドウで、**構成の作成** を選択します。
3. ドロップダウン ダイアログ ボックスで、**名前から派生した税計算サービス、Microsoft** を選択し、新しい税の構成の名前を入力し、**コンフィギュレーションの作成** を選択します。
4. 作成した税コンフィギュレーションを選択し、アクション ウィンドウで **デザイナー** を選択します。
5. **プロパティ** セクションの **データ モデル** フィールドで、先に作成したカスタマイズされた税データ モデルを選択します。
6. **データ モデル バージョン** フィールドで、税データ モデルの完成したバージョンを選択します。
7. **追加** を選択し、必要な税対策を追加します。
8. アクション ウィンドウで、**保存** を選択してから、**完了** を選択します。
9. ページを閉じて、完成したバージョンの税の構成を表示します。

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>カスタマイズされた税コンフィギュレーションでの税機能の実装

1. Regulatory Configuration Service (RCS) で、**グローバリゼーション機能** > **税** に移動します。
2. **追加** を選択し、新しい機能に関する情報を入力し、**機能の作成** を選択します。
3. **バージョン** タブで機能を選択し、**編集** を選択します。
4. **全般** タブの **コンフィギュレーション バージョン** フィールドで、カスタマイズされた税コンフィギュレーションおよびバージョンを選択します。
5. **列の管理** ダイアログ ボックスで、カスタマイズした税対策に含めるヘッダーおよび行の列を選択し、右矢印ボタンを選択して **選択した列** リストに追加します 。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
