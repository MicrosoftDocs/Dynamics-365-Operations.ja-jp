---
title: Dynamics 365 Commerce での実験
description: 実験により、サイト ビルダーでのページ レイアウトの作成、編集、管理、およびコンテンツの処理が可能になります。 エンド ツー エンドの実験サポートは、E コマース ページおよびページ内のエンティティに対して有効になります。
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 85eb7a661cc66c42699797cca4fa6820941de7c0
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2020
ms.locfileid: "4413892"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Dynamics 365 Commerce での実験
Dynamics 365 Commerce での実験を使用して、E コマース ページの有効性についての仮想を検証し、データ駆動型信頼とともに決定を行います。 Commerce では、ページ、モジュール、およびフラグメントの A/B テストをサポートしており、Web サイトに提案された変更の影響を測定できます。

コマース サイト ビルダーでは、ページの作成、編集、管理および **バリエーション** と呼ばれるコンテンツの処理を行なえます。 Commerce は、実験や処理の割り当てを作成するために使用できるサード パーティ サービスと統合します。 Commerce でキャプチャされた Real-time イベント ストリームは、サード パーティ サービスで実験結果を定義する分析を有効にします。 その後、仮想のサポートまたは反論を支援するために、これらの分析を活用できます。

## <a name="set-up-prerequisites"></a> 前提条件の設定
1. **Commerce の適切なバージョンの入手** - モジュール ライブラリ、オンライン チャネル拡張ソフトウェア開発キット (SDK)、および Commerce Scale Unit を Commerce バージョン 10.0.13 以降にアップグレードします。
1. **実験コネクタの設定** - 実験コネクタは、Commerce がサード パーティ サービスと接続して実験のリストを取得し、実験をユーザーに対して表示するタイミングを決定することができます。 サード パーティ コネクタは、[AppSource](https://appsource.microsoft.com) から購入できます。 発行元が提供する設定手順に従ってください。 あるいは、Commerce からのサンプル テスト コネクタを使用して、外部サービスを構成する必要なく、実験ワークフローをテストすることもできます。 詳細については、[コネクタのコンフィギュレーションと有効化](e-commerce-extensibility/connectors.md)を参照してください。 
1. **Commerce で実験機能のフラグをオンにする** - テナント レベルでの実験を有効にするには、**テナントの設定 > 機能** または **サイト設定 > 機能** のサイト レベルに移動します。
    - 実験の一部ではない他のコンテンツに影響を与えたりコピーしたりせずに、ページ内にモジュールの実験バリエーションを作成するために **実験** フラグを有効にします。 これにより、実験のライフサイクルの間、実験外で進行中のコンテンツの更新は確実に同期を維持します。 このフラグを無効にすると、すべての実験がユーザーに表示されなくなり、サイト ビルダー内のすべての編集機能が削除されます。
    - ページまたはフラグメントでの実験を実行するために、**ページまたはフラグメントでの実験** フラグを有効にします。 これにより、ページまたはフラグメント内のページ全体のフル インスタンス コピーまたはすべてのモジュールのフラグメントが作成されます。 包括的なコンテンツの変更をテストする場合、またはインスタンス間で進行中のコンテンツの変更を同期することが問題にならない場合に使用します。 このフラグを無効にすると、ページおよびフラグメントの新しい実験を作成および編集ができなくなります。
    > [!NOTE]
    > **ページまたはフラグメントでの実験** 機能の実行には、**実験** フラグを有効にする必要があります。
    
## <a name="experimentation-lifecycle"></a>実験ライフサイクル
実験の設定、バリエーションの作成、および実験の実行は、反復プロセスです。 次の図は、Commerce およびサード パーティ サービスでの実験ライフサイクルを示しています。 

[ ![実験ライフサイクル](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

実験プロセスの各手順の詳細については、次のトピックを参照してください。
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