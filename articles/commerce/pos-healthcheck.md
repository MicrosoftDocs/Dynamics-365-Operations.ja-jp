---
title: POS 周辺機器およびサービスの正常性チェック
description: このトピックは、販売時点管理 (POS) での正常性チェックの操作概要を提供します。
author: rubendel
manager: AnnBe
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 86f0964b6d929d0434a8bf04aaefc173bee21c6f
ms.sourcegitcommit: d77e902b1ab436e5ff3e78c496f5a70ef38e737c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2020
ms.locfileid: "4413877"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>POS 周辺機器およびサービスの正常性チェック

[!include [banner](includes/banner.md)]

このトピックは、販売時点管理 (POS) での正常性チェックの操作概要について説明します。

## <a name="overview"></a>概要

小売店舗は、多くのアプリケーションとデバイスが使用される複雑な環境になることがあります。 たとえば、周辺機器が故障したり、誤って 1 日中プラグが外れるなど、相互関係のため、操作が増えると常に操作をスムーズに実行するのが困難になることがあります。 デバイスやサービスに関係する問題のトラブルシューティングは、大きな商社には費用がかかり、小さな操作ゆえに均等にもどかしくなることがあります。

Microsoft Dynamics 365 Commerce バージョン 10.0.10 以降には、このような費用とフラストレーションを回避するのに役立つ正常性チェックの操作が含まれています。 通常の操作以外のこの操作により、POS からデバイスを直接テストする方法が提供されます。 したがって、小売業者は問題が発生する前に検出することができます。

## <a name="key-terms"></a>重要な用語

| 期間 | 説明 |
|---|---|
| 周辺機器 | POS アプリケーションが使用するすべてのデバイスにより、店舗のトランザクションおよび他の操作が容易になります。 例には、キャッシュ ドロワー、バーコード スキャナー、支払ターミナルなどがあります。 |
| サービス | このトピックでは、サービスは POS アプリケーションが依存する付加的なアプリケーションのことで、トランザクションおよび日常業務を実行します。 例には、税または出荷計算に役立つアプリが含まれます。 |

## <a name="health-check-operation"></a>正常性チェック操作

正常性チェックの操作は、Commerce 本社の **POSの操作** ページの操作 717 です。 POS が非ドロワーモードの場合に使用できます。 ただし、ハードウェア ステーションが有効である必要があります。

既定では、正常性チェックは、現在レジスターに有効になっているハードウェア ステーションに対してハードウェア プロファイルでコンフィギュレーションされているデバイスのみをテストします。 レジスターが 1 日中複数のハードウェア ステーションを使用していて、すべてに対して正常性チェックを行う場合、、一度に 1 つのハードウェアステーションに接続する必要があります。 店舗レベルの正常性チェックはありません。 ただし、このタイプのチェックは、Commerce サーバーの拡張機能により実行することが可能です。

### <a name="out-of-box-health-checks"></a>最初から用意されている正常性チェック

| 種類 | 接続 | 詳細情報 |
|---|---|---|
| プリンター | OPOS | このチェックは、POS (OPOS) 機能にリンクおよび埋め込まれている基本的なオブジェクトをテストします。 次にいくつか例を挙げます。<ul><li>開く: **開く** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>閉じる: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| ライン ディスプレイ | OPOS | このチェックは、基本的な OPOS 機能をテストします。 次にいくつか例を挙げます。<ul><li>開く: **開く** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>閉じる: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| デュアル ディスプレイ | Windows | このチェックにより、オペレーティング システムが 2 番目の Windows ディスプレイを検出できるようになります。 | 
| MSR | OPOS | このチェックは、基本的な OPOS 機能をテストします。 次にいくつか例を挙げます。<ul><li>開く: **開く** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>閉じる: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| 手形振出人 | OPOS | このチェックは、基本的な OPOS 機能をテストします。 次にいくつか例を挙げます。<ul><li>開く: **開く** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>閉じる: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> | 
| スキャナー | OPOS | このチェックは、基本的な OPOS 機能をテストします。 次にいくつか例を挙げます。<ul><li>開く: **開く** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>閉じる: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> | 
| スケール | OPOS | このチェックは、基本的な OPOS 機能をテストします。 次にいくつか例を挙げます。<ul><li>開く: **開く** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>閉じる: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| PIN パッド | OPOS | このチェックは、基本的な OPOS 機能をテストします。 次にいくつか例を挙げます。<ul><li>開く: **開く** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>閉じる: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| 支払ターミナル | 支払の SDK | このチェックは、支払 SDK によって提供される基本的な支払ターミナルの機能をテストします。 <ul><li>ロック</li><li>BeginTransaction</li><li>EndTransaction</li><li>ReleaseDevice</li><li>精算</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>POS での正常性チェック操作の使用

POS で正常性チェック操作が開始されると、コンフィギュレーションされたデバイスの一覧と各デバイスの状態が右側のウィンドウに表示されます。 単一のデバイスに対して正常性チェックを行うには、デバイスを選択して、**選択先をテスト** を選択します。 すべてのデバイスに対して正常性チェックを行うには、**すべてテスト** を選択します。 **すべてテスト** 機能は、すべてのデバイスを一度に 1 つずつテストし、**状態** 列の各デバイスの状態を更新します。

**最後のチェック** 列には、各デバイスに対して正常性チェックがいつ最後に行われたかが表示されます。

デバイスの正常性チェックに合格した場合 (つまり、エラーが発生しなかった場合)、デバイスの状態は **OK** になります。 正常性チェックが失敗した場合、状態はエラーが発生したことを示します。 この場合、右のウィンドウにエラーに関係する詳細が表示されるか、またはシステム管理者に連絡するようユーザーに指示されます。

OPOS キーロックなどの一部のデバイスには、最初から用意されている正常性チェック テストはありません。 使用されているすべてのデバイスについて正常性チェック テストが検出されなかった場合、状態は **サポートされていません** になります。

### <a name="extending-health-checks"></a>正常性チェックの拡張

最初から用意されている正常性チェック テストは、一般的なエラーに対してわかりやすいメッセージを提供するようにコンフィギュレーションされています。 ただし、すべてのシナリオが対象になっているわけではありません。 拡張機能によって、商社は環境に特有のエラーに対して分かりやすいメッセージをマップできます。

カスタム正常性チェックを作成して、最初はサポートされていなかったデバイスのテスト、または POS が依存するすべてのサービスをテストすることもできます。

## <a name="related-articles"></a>関連記事

[Modern POS (MPOS) のトリガーと印刷](dev-itpro/pos-trigger-printing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]