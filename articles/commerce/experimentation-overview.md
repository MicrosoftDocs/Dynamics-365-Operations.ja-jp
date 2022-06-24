---
title: Dynamics 365 Commerce での実験
description: 実験により、サイト ビルダーでのページ レイアウトの作成、編集、管理、およびコンテンツの処理が可能になります。 エンド ツー エンドの実験サポートは、E コマース ページおよびページ内のエンティティに対して有効になります。
author: sushma-rao
ms.date: 06/07/2022
ms.topic: overview
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1ef877072ba7ffe1b0326cf8d526b512b5ab30b8
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946217"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Dynamics 365 Commerce での実験
Dynamics 365 Commerce での実験を使用して、E コマース ページの有効性についての仮想を検証し、データ駆動型信頼とともに決定を行います。 Commerce では、ページ、モジュール、およびフラグメントの A/B テストをサポートしており、Web サイトに提案された変更の影響を測定できます。

コマース サイト ビルダーでは、ページの作成、編集、管理および **バリエーション** と呼ばれるコンテンツの処理を行なえます。 Commerce は、実験や処理の割り当てを作成するために使用できるサード パーティ サービスと統合します。 Commerce でキャプチャされた Real-time イベント ストリームは、サード パーティ サービスで実験結果を定義する分析を有効にします。 その後、仮想のサポートまたは反論を支援するために、これらの分析を活用できます。

## <a name="set-up-prerequisites"></a> 前提条件の設定

1. **Commerce の適切なバージョンの入手** - モジュール ライブラリ、オンライン チャネル拡張ソフトウェア開発キット (SDK)、および Commerce Scale Unit を Commerce バージョン 10.0.13 以降にアップグレードします。
1. **実験コネクタの設定** - 実験コネクタは、Commerce がサード パーティ サービスと接続して実験のリストを取得し、実験をユーザーに対して表示するタイミングを決定することができます。 サード パーティ コネクタは、[AppSource](https://appsource.microsoft.com) から購入できます。 発行元が提供する設定手順に従ってください。 あるいは、Commerce からのサンプル テスト コネクタを使用して、外部サービスを構成する必要なく、実験ワークフローをテストすることもできます。 詳細については、[コネクタのコンフィギュレーションと有効化](e-commerce-extensibility/connectors.md)を参照してください。 
1. **Commerce で実験機能のフラグをオンにする** - 実験を有効にするには、**テナントの設定 \> 機能** へ移動してテナント レベルで行うか、**サイト設定 \> 機能** へ移動してサイト レベルで行うことができます。 **実験** フラグをオンにして、モジュール バリエーションの作成を開始します。 このフラグを無効にすると、すべての実験がユーザーに表示されなくなり、サイト ビルダー内のすべての編集機能が削除されます。
    
## <a name="experimentation-lifecycle"></a>実験ライフサイクル

実験の設定、バリエーションの作成、および実験の実行は、反復プロセスです。 次の図は、Commerce およびサード パーティ サービスでの実験ライフサイクルを示しています。 

[ ![実験ライフサイクル。](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

実験プロセスの各手順の詳細については、次の記事を参照してください。
- [仮説を識別して実験のメトリックスを決定する](experimentation-identify.md)
- [実験の設定](experimentation-setup.md)
- [接続して実験を編集する](experimentation-connect-edit.md)
- [実験のプレビューと発行](experimentation-preview-publish.md)
- [実験の実行と監視](experimentation-run-monitor.md)
- [バリエーションのレベルを上げて実験を完了する](experimentation-review-complete.md)

> [!NOTE]
> 実験がライフサイクルのどこにあるかを知るには、サイト ビルダーの左側ナビゲーション ペインにある **実験** を選択します。 実験のリストが、Commerce およびサード パーティ サービス両方の各実験のステータスと共に表示されます。 詳細については、[実験のステータスを確認する](experimentation-status.md)を参照してください。

## <a name="next-step"></a>次のステップ
[仮想を識別して実験の成功メトリックを決定する](experimentation-identify.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
