---
title: Dynamics 365 Retail バージョン 10.0.6 の新機能および変更された機能
description: このトピックでは Dynamics 365 Retail のプレビュー中の機能について説明します。
author: josaw1
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 84e3bf751b9360c943d1ee3b2a1fe72bf65b495e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797158"
---
# <a name="whats-new-or-changed-in-dynamics-365-retail-version-1006"></a>Dynamics 365 Retail バージョン 10.0.6 の新機能および変更された機能

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Retail 10.0.6 の新機能または変更された機能について説明します。 

Finance and Operations アプリケーションの機能については、[Finance and Operations アプリ バージョン 10.0.6 (2019 年 11 月) の新機能と変更点](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-10-0-6) を参照してください。

## <a name="new-inventory-availability-apis-for-e-commerce-use"></a>E コマース用の新しい引当可能在庫数 API
4 つの新しい API が利用可能になり、E コマースまたはサード パーティのソリューションに、要求された品目と倉庫に対する手持在庫の見積を提供します。  これらの API は、現在市場にある既存の GetProductAvailabilities および GetAvailableInventoryNearby API と置き換えることを目的としています。   これらの新しい API では、パフォーマンスを向上させるための計算ロジックとキャッシングが向上します。  新しい API の名前は次のとおりです。
* GetEstimatedProductWarehouseAvailability
* GetEstimatedAvailabilityDefaultWarehouse
* GetEstimatedAvailabilityNearby
* GetEstimatedAvailabilityAllWarehouses

また、チャネル データベースで利用可能な E コマースの在庫を追跡するための新しいテーブルが追加されました。  Retail および小売用の共有パラメーターが利用可能になります。以前のバージョンに存在していた既存の高価な E コマース引当可能在庫数ロジックを無効にするこれらの新しい API とテーブルを取得するよう、それらをコンフィギュレーションする必要があります。

### <a name="install-merchant-properties-deprecated-from-the-hardware-station-installer"></a>ハードウェア ステーション インストーラーからのマーチャント プロパティのインストールは推奨されません。
ヘッドレス インストールの将来の拡張機能をより適切にサポートするため、ハードウェア ステーション インストール操作からマーチャント プロパティ インストーラーが削除されました。 10.0.6 の新機能として、ハードウェア ステーションのマーチャント プロパティは必要に応じて、POS をハードウェア ステーションとペアリングされる際の実行時に設定され、ハードウェア ステーションが有効になるときに更新されます。 POS とハードウェア ステーションの両方が同時に 10.0.6 に更新されていない場合、POS によるマーチャント プロパティの設定と更新は正しく機能しません。 つまり、ハードウェア ステーションでなく POS が更新された場合、ハードウェア ステーションが更新されるまで古いマーチャント プロパティを引き続き使用することを意味します。 

## <a name="additional-resources"></a>追加リソース

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2019 リリース ウェーブ 2 プラン](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/index) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]