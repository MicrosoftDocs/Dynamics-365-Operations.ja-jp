---
title: コマースの周辺機器の互換性
description: このトピックでは、Dynamics 365 Commerce との互換性のテストが完了している周辺機器を示します。
author: BrianShook
ms.date: 11/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-10-08
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02a380623bbcd96ae6dfb4739007f2466435c3db
ms.sourcegitcommit: 971456c197820421f108ad7345001cc1b6c99949
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/01/2021
ms.locfileid: "7875434"
---
# <a name="peripheral-compatibility-for-commerce"></a>コマースの周辺機器の互換性

[!include [banner](../includes/banner.md)]

このページに挙げられたデバイスでは、[コマースの周辺機器シミュレーター](dev-itpro/retail-peripheral-simulator.md) を使用して Dynamics 365 Commerce との互換性のテストが完了しています。 デバイスごとに、テストを実行し、Microsoft に成功結果を送信した関係者が、[テスト担当者] 列に表示されます。 "Microsoft Corp" によるテストとして表示されているデバイスについては、Microsoft にサポート要求を送信する必要があります。 Microsoft 以外の関係者によってテストされたデバイスに関する問題は、まずテストした関係者に報告する必要があります。

## <a name="compatible-devices-by-type"></a>タイプ別の互換性のあるデバイス

### <a name="line-display"></a>ライン ディスプレイ

| テスト日 | テスト担当者 | メーカー | メーカーの Web サイト | サポート メール | サポート電話番号 | モデル名 | 運転者名 | ドライバー バージョン | ファームウェア バージョン | ドライバーの種類 | 接続 | ドライバー ダウンロード リンク |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 2017/10/17 | HP | HP | https://www.hp.com | support@hp.com | | HPTD620Display | HPTD620Display | 6.6.5.6 | 1.02.11 | OPOS | USB | https://www.hp.com |

### <a name="msr"></a>MSR

| テスト日 | テスト担当者 | メーカー | メーカーの Web サイト | サポート メール | サポート電話番号 | モデル名 | 運転者名 | ドライバー バージョン | ファームウェア バージョン | ドライバーの種類 | 接続 | ドライバー ダウンロード リンク |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 2017/10/17 | HP | HP | https://www.hp.com | support@hp.com | | HPSinglenoSRDMSR | HPSinglenoSRDMSR | 3.29 | 5.37 | OPOS | USB | https://www.hp.com |

### <a name="printer"></a>プリンター

| テスト日 | テスト担当者 | メーカー | メーカーの Web サイト | サポート メール | サポート電話番号 | モデル名 | 運転者名 | ドライバー バージョン | ファームウェア バージョン | ドライバーの種類 | 接続 | ドライバー ダウンロード リンク |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 2017/10/17 | HP | HP | https://www.hp.com | support@hp.com | | H300 | H300 | 1.14.1.19 | 1.61B | OPOS | USB | https://www.hp.com |

### <a name="bar-code-scanner"></a>バーコード スキャナー

| テスト日 | テスト担当者 | メーカー | メーカーの Web サイト | サポート メール | サポート電話番号 | モデル名 | 運転者名 | ドライバー バージョン | ファームウェア バージョン | ドライバーの種類 | 接続 | ドライバー ダウンロード リンク |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 2017/10/17 | HP | HP | https://www.hp.com | support@hp.com | | N3680-HP | N3680-HP | 1.14.0.5 | DX000010BAA | OPOS | USB | https://www.hp.com |

> [!NOTE]
> この互換性リストは、2018 年 9 月現在最新です。 デバイスが正常にテストされ、結果が Microsoft に送信されるにつれて、リストは徐々に増加します。

## <a name="device-compatibility-testing"></a>デバイス互換性テスト

デバイスの互換性は、周辺機器シミュレーターを使用してテストできます。 周辺機器シミュレーターの入手、デバイスのテスト、および Microsoft に送信するためのテスト ログを生成する方法に関する詳細については、[コマースの周辺機器シミュレーター](dev-itpro/retail-peripheral-simulator.md)を参照してください。 実稼働環境に送られるすべての周辺機器設定に対してテストを実行する必要があります。 互換性リストが、過去にまったく同じデバイス/POS 設定でテストされていることを示している場合でも、ユーザー受け入れテスト (UAT) の一環としてテストを行う必要があります。

## <a name="supported-devices"></a>サポート対象デバイス

既に互換性がテストされて Microsoft に結果が送信されたデバイスのみ、新しい実装でサポートされます。 これは、新しい実装が適切にテストされ、以前にテストされたデバイスのライブラリを作成するために必要です。 以前は、Microsoft がデバイスで内部テストを実施し、結果が [周辺機器](retail-peripherals-overview.md) などの適切な場所に掲載されていました。 市場のデバイスにはさまざまなバリエーションがあるため、このプロセスでは対応できません。 そのため、今後は、テストの大半をパートナー、お客様、および (最も重要な点として) デバイスの製造元が行う必要があります。 原則的には、パートナーやお客様が互換性のあるデバイスの一覧に基づいて周辺機器を選択できるように、デバイスは製造元により事前にテストされます。

## <a name="disclaimer"></a>免責事項

© 2018 Microsoft Corporation. All rights reserved

このドキュメントに記載された内容は情報提供のみを目的としており、これらの情報についてマイクロソフトは明示、黙示、あるいは法律上のいかなる責任も負わないものとします。 結果は、指定した Microsoft Dynamics ソフトウェアが使用された制御されているラボ環境での、特定のデバイスおよびコンフィギュレーションのテストに基づいています。 異なるシステム ハードウェア、ソフトウェア デザインまたはコンフィギュレーション、カスタマイズ、またはトランザクションの組み合わせによって、実際のパフォーマンスまたは結果に影響が及ぶ場合もあります。

MICROSOFT は、明示的または暗黙的にかかわらず、この概要を保証を行いません。 このドキュメントは、"現状のまま" 提供されます。 URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。 このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。 このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。 内部での参照を目的とする場合、このドキュメントをコピーして使用できます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
