---
title: Hardware Station 拡張性
description: このトピックでは、新規デバイスと既存デバイスの新規デバイス タイプのサポートを追加するために、Hardware Station を拡張する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 17971
ms.assetid: 256f7f2b-c419-442f-b195-0c6a299a056e
ms.search.region: Global
ms.author: sijoshi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ae5f24d55846fc242be5435f7893e85d66e04e75
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537603"
---
# <a name="hardware-station-extensibility"></a>Hardware Station 拡張性

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> このトピックは、Dynamics 365 for Finance and Operations バージョン 7.1 およびそれ以前のバージョンに適用されます。 バージョン 7.2 およびそれ以上の場合は、この実装はサポートされていません。 これらのバージョンでは、オーバーレイせずに拡張モデルに従います。

このトピックでは、新規デバイスと既存デバイスの新規デバイス タイプのサポートを追加するために、Hardware Station を拡張する方法について説明します。

<a name="retail-hardware-station-overview"></a>Retail Hardware Station の概要
--------------------------------

Retail Hardware Station は、プリンター、キャッシュ ドロワー、スキャナー、および支払ターミナルなどの小売ハードウェア周辺機器に接続するために Retail Modern POS および Cloud POS で使用されます。 

[![HWS-Local-Traditional](./media/hws-local-300x236.png)](./media/hws-local.png)

[![HWS-Shared](./media/hws-shared-300x224.png)](./media/hws-shared.png)

## <a name="retail-hardware-station-setup"></a>Retail Hardware Station の設定
開始する前に、[Retail ハードウェア ステーションのコンフィギュレーションとインストール](../retail-hardware-station-configuration-installation.md)の情報を使用してハードウェア ステーションをインストールし、ハードウェアがどのようなものでインストールがどのようにされているかを知ることができます。

## <a name="retail-hardware-station-architecture"></a>Retail Hardware Station アーキテクチャ
ハードウェア ステーションは、ハードウェア ステーション アプリケーション プログラミング インターフェイス (API) 用の Web API を公開します。 新しいデバイス (たとえば、現金自動支払機) の新しいコントローラーを実装するか、または既存のデバイス タイプ (たとえば、新しいオーディオ ジャック磁気ストライプ リーダー (MSR) の実装) の既存のコント ローラーを上書きするかのいずれかによって、ハードウェア ステーションを拡張できます。

[![ハードウェア ステーション アーキテクチャ](./media/hardware-station-architecture-1024x764.png)](./media/hardware-station-architecture.png)

## <a name="retail-hardware-station-extensibility-scenarios"></a>Retail Hardware Station 拡張性シナリオ
.NTE にサポートされている [Managed Extensibility Framework (MEF)](https://msdn.microsoft.com/en-us/library/dd460648(v=vs.110).aspx) を使用して、ハードウェア ステーションの拡張性が獲得されます。 **拡張性の規定:** 拡張機能アセンブリで、常に、拡張機能の書き込みをします。 そのようにして、実際の拡張機能を記述し、アップグレードがかなり簡単になります。 拡張のための 2 つの基本的なシナリオがあります。

-   **新しいデバイスを追加する** - 最初から用意されているハードウェア ステーションはデバイス (現金自動支払機など) をまだサポートしていません。 したがって、ハードウェア ステーションで新しいデバイスのサポートを追加する必要があります。
-   **既存のデバイスに対する新しいデバイス タイプを追加する** - 最初から用意されているハードウェア ステーションの実装ではすでにデバイス (MSR など) がサポートされていますが、特定のデバイス タイプ (オーディオ ジャック MSR 実装) のサポートを追加する必要があります。

### <a name="scenario-1-adding-a-new-device"></a>シナリオ 1: 新しいデバイスを追加する

このシナリオでは、ハードウェア ステーションで、現金自動支払機装置のサポートを追加します。 ここでは、メモ帳ファイルで現金を分配する疑似現金自動支払機を作成します。 ただし、この例はハードウェア ステーションのエンド ツー エンドの拡張機能を理解するのに役立ちます。

-   Retail ソフトウェア開発キット (SDK) には、現金自動支払機のサンプルがあります。 RetailSdk\\SampleExtensions\\HardwareStation を参照してください。
-   この場合、新しい Web API コントローラーおよびヘルパー プロパティ/メソッドを追加する必要があります。
-   新しい **CashDispenser** コントローラーは、**ApiController** と **IHardwareStationController** を拡張する必要があります。
-   ここの **エクスポート** 属性文字列は、このコントローラーが使用されるデバイスを指定します: \[Export("CASHDISPENSER", typeof(IHardwareStationController))\]

<!-- -->

    namespace Contoso
    {
        namespace Commerce.HardwareStation.CashDispenserSample
        {
            using System;
            using System.Composition;
            using System.Web.Http;
            using Microsoft.Dynamics.Commerce.HardwareStation;
            using Microsoft.Dynamics.Retail.Diagnostics;
            /// <summary>
            /// Cash dispenser web API controller class.
            /// </summary>
            [Export("CASHDISPENSER", typeof(IHardwareStationController))]
            public class CashDispenserController : ApiController, IHardwareStationController
            { 
                // Add your controller code here
            }

### <a name="scenario-2-adding-a-new-device-type-for-an-existing-device"></a>シナリオ 2: 既存のデバイスの新しいデバイス タイプを追加する

このシナリオでは、既存のデバイス (オーディオ ジャック MSR 実装) に対する新しいデバイス タイプのサポートを追加します。

-   **エクスポート** 属性文字列は、このコントローラーが使用されるデバイスを指定します: \[Export("MSR", typeof(IHardwareStationController))\]
-   MSR に対して複数のコントローラーが存在するため、ハードウェア ステーションは構成ファイルを使用して実行時にどの実装を使用するかを決定します。 詳細については、この記事の後半の「Retail ハードウェア ステーションの拡張機能コンフィギュレーション」セクションを参照してください。

<!-- -->

    namespace Contoso
    {
        namespace Commerce.HardwareStation.RamblerService
        {
            using System;
            using System.Composition;
            using System.Threading.Tasks;
            using System.Web.Http;
            using System.Web.Http.Controllers;
            using Microsoft.Dynamics.Commerce.HardwareStation;
            using Microsoft.Dynamics.Commerce.HardwareStation.DataEntity;
            using Microsoft.Dynamics.Commerce.HardwareStation.Models;
            using Microsoft.Dynamics.Retail.Diagnostics;
            /// <summary>
            /// MSR device web API controller class.
            /// </summary>
            [Export("MSR", typeof(IHardwareStationController))]
            [Authorize]
            public class AudioJackMSRController : ApiController, IHardwareStationController
            {
                // Add controller implementation here
            }

## <a name="retail-hardware-station-extensibility-configuration"></a>Retail Hardware Station 拡張性コンフィギュレーション
### <a name="configuration-for-iis-hosted-hardware-station"></a>IIS でホストされているハードウェア ステーションのコンフィギュレーション

ハードウェア ステーションが拡張機能を使用する前に、拡張機能のエントリが含まれるようにハードウェア ステーション Web.config ファイルの**合成**セクションを更新する必要があります。 コンフィギュレーション ファイルの構成ターゲットの順序によって優先順位が決まります。 

[![ハードウェア ステーション Web コンフィギュレーション](./media/hws-webconfig.png)](./media/hws-webconfig.png)

### <a name="configuration-for-local-ipc-based-hardware-station"></a>ローカル IPC ベースのハードウェア ステーションのコンフィギュレーション

ローカルのハードウェア ステーションが拡張機能を使用する前に、拡張機能用のエントリが含まれるように Modern POS DllHost.exe.config ファイル (C:\\Program Files (x86)\\Microsoft Dynamics AX\\70\\Retail Modern POS\\ClientBroker) の**合成**セクションを更新する必要があります。 コンフィギュレーション ファイルの構成ターゲットの順序によって優先順位が決まります。

[![ローカル ハードウェア ステーションのコンフィギュレーション](./media/hws-dll-host-local-config.png)




