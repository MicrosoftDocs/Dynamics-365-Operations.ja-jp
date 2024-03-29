---
title: 倉庫管理概要
description: 倉庫プロセスを監視および自動化するために、倉庫管理を使用します。
author: Mirzaab
ms.date: 04/20/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters, WHSWorkPool
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d22ed879f309c0fbb999bf166aefd13f27376042
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069095"
---
# <a name="warehouse-management-overview"></a>倉庫管理の概要

[!include [banner](../includes/banner.md)]

倉庫管理モジュールは、製造、配送、および小売企業の倉庫プロセスを管理できます。 このモジュールは、倉庫施設をいつでも最適なレベルにサポートする幅広い機能を持っています。 倉庫管理では、輸送、製造、品質テスト、購買、移動、販売、返品などの他のビジネス プロセスが完全に統合されます。

## <a name="get-started"></a>使用開始
倉庫管理の操作を開始するには、会社の業務プロセスをサポートするための通常倉庫のパラメーターの設定を完了する必要があります。

- **倉庫管理** > **設定** ページ下の **倉庫管理パラメーター** に移動し、通常倉庫のパラメーターの設定をします。

業務要件に従って入庫/出庫の倉庫プロセスワークフローをコンフィギュレーションする必要があります。 コンフィギュレーションする必要がある最も重要なコンポーネントは、ウェーブ テンプレート、作業テンプレート、作業プールと場所のディレクティブです。

- [倉庫のコンフィギュレーションの概要](warehouse-configuration.md)
- [作業テンプレートと場所ディレクティブを使用した倉庫作業の制御](control-warehouse-location-directives.md)
- [倉庫作業用のモバイル デバイスの設定](configure-mobile-devices-warehouse.md)
- [発注書のプット アウェイ場所のディレクティブの設定](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [発注書の作業テンプレートの設定](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes-wms"></a>倉庫管理プロセス (WMS)
- 販売注文、返品、移動オーダー、製造オーダー、およびかんばんの元伝票の統合されたサポート  
- 変動、入庫、出庫材料ワークフローサポートはクエリに基づいています
- 製造、および輸送管理提供との完全な統合
- 在庫限度と場所の容積測定をフルコントロール
- 在庫状態によって管理された在庫プロパティ
- 完全バッチとシリアル品目サポート
- さまざまな品目の入荷能力
- 積荷の複数ピッキング
- 次世代バー コード スキャナーのサポート
- 倉庫プロセスのパレット/コンテナーのタイプ
- 高度な棚卸能力
- Zebra ZPL サポートでラベルの印刷およびラベル ルート指定
- ビジネス インテリジェンスの Power BI への統合
- 在庫の手動、および自動移動
- 完全に統合された品質テスト (QMS)
- 作業者の材料取り扱いの完全なトレーサビリティ
- 出荷ウェーブ処理
- 手動の梱包と自動のコンテナ詰めをサポート
- クラスター ピッキング
- シンプルクロスドッキング

## <a name="additional-resources"></a>追加リソース
### <a name="whats-new-and-in-development"></a>新機能および開発中の機能
リリースされた新機能と開発中の新機能については、[Microsoft Dynamics 365 ロードマップ](https://roadmap.dynamics.com/) を参照してください。

### <a name="blogs"></a>ブログ
倉庫管理およびその他のソリューションに関する意見、ニュース、その他の情報については、「[Microsoft Dynamics 365 ブログ](https://community.dynamics.com/b/msftdynamicsblog)」を参照してください。


 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]