---
title: Dynamics 365 Commerceコンポーネント バージョンの管理要件
description: このトピックでは、Microsoft Dynamics 365 Commerce エコシステムのすべてのコンポーネントに対する、コンポーネント バージョン要件および依存関係の概要について説明します。
author: rezaassadi
manager: AnnBe
ms.date: 07/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailITWorkspace
audience: Developer, IT Pro
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 02cb1bf662983edb74ad5173e2c494a0edfe8d3f
ms.sourcegitcommit: 267498fbc4c54adf83b15854ecea6a93e200164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/09/2020
ms.locfileid: "3549337"
---
# <a name="dynamics-365-commerce-component-versioning-requirements"></a>Dynamics 365 Commerceコンポーネント バージョンの管理要件

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce エコシステムのすべてのコンポーネントに対する、コンポーネント バージョン要件および依存関係の概要について説明します。

## <a name="overview"></a>概要

次の図は、Dynamics 365 Commerce コンポーネントの概要、それに対応するバージョン要件および依存関係を示しています。

<a href="https://docs.microsoft.com/en-us/dynamics365/commerce/media/commerce-component-versioning.jpg" target="_blank">![Dynamics 365 Commerce コンポーネント バージョン要件および依存関係](./media/commerce-component-versioning.jpg)</a>

## <a name="component-dependencies"></a>コンポーネントの依存関係

### <a name="service-updates"></a>サービスの更新

顧客およびパートナーがサービスおよび配置を行うすべてのコマース コンポーネントとの互換性を確保するには、更新サービス中にいくつかのバージョン依存関係に従う必要があります。 次のリストは、これらの依存関係をすべて示しています。

- **コマースの本部と Finance and Operations アプリは、Commerce Scale Unit (クラウドと自己ホスト型の両方) と同じバージョンか、それよりも新しいバージョンになっている必要があります。**

    たとえば、コマースの本部と Finance and Operations アプリがバージョン 10.0.10 である場合、Commerce Scale Unit はバージョン 10.0.10 またはそれ以前 (たとえば、10.0.9 または 10.0.8) である必要があります。

- **Commerce Scale Unit は、Modern Point of Sale (POS)、Hardware Station、コマース ソフトウェア キット (SDK) と同じバージョンかそれより新しいバージョン、および関連するローカル サイト コンフィギュレーション (モジュール、データ アクション、テーマなど) でなくてはなりません。**

    たとえば、Commerce Scale Unit がバージョン 10.0.10 である場合、Modern POS、Hardware Station、およびコマース ストアフロントはバージョン 10.0.10 またはそれ以前 (たとえば、10.0.9 または 10.0.8) である必要があります。

- **拡張機能パッケージは、拡張機能が適用されるターゲット コンポーネントと同じバージョン、またはそれより新しいバージョンに対してコンパイルする必要があります。**

    たとえば、展開された Commerce Scale Unit がバージョン 10.0.10 である場合、対応する拡張パッケージをバージョン 10.0.10 またはそれ以前のバージョン (たとえば、10.0.10 または 10.0.9) に対してコンパイルする必要があります。

### <a name="quality-updates"></a>品質更新プログラム

品質更新プログラム中、サービス更新プログラムに必要なもの以外に、各コマース コンポーネントに対して特定のバージョン管理要件に従う必要はありません。

## <a name="current-supported-versions"></a>現在サポートされているバージョン

次の表では、**2020 年 7 月 1 日**時点での各種コマース コンポーネントの現在のサポートされているバージョンを示します。

| コンポーネント | 最新の利用可能なリリース | 最新の使用可能なコンポーネントのバージョン番号 | サポートされている最も古いリリース | サポートされている最も古いコンポーネントのバージョン番号 |
|---|---|---|---|---|
| Finance and Operations アプリ | 10.0.12 | 10.0.12 | 10.0.9 | 10.0.9 |
| Commerce Scale Unit (クラウド自己ホスト) | 10.0.12 | 9.22 | 10.0.9 | 9.19 |
| Commerce ストア スターター キット (SSK) | 10.0.12 | 9.22 | 10.0.9 | 9.22 |
| Commerce Scale Unit (自己ホスト) | 10.0.12 | 9.22 | 10.0.5 | 9.15 |
| Modern POS | 10.0.12 | 9.22 | 10.0.5 | 9.15 |
| ハードウェア ステーション | 10.0.12 | 9.22 | 10.0.5 | 9.15 |

## <a name="one-version-requirements"></a>1 つのバージョン要求

コマース コンポーネントは、2018 年 7 月に発表された同じ [1 つのバージョン サービスの更新プログラム](https://cloudblogs.microsoft.com/dynamics365/bdm/2018/07/06/modernizing-the-way-we-update-dynamics-365/)、およびその後 2019 年 6 月に発表され公開された [Finance and Operations アプリの柔軟なサービスの更新プログラム](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/06/03/new-flexible-service-updates-for-dynamics-365-for-finance-and-operations/) も追従しています。 詳細については、[1 つのバージョン サービスに関してよく寄せられる質問](../fin-ops-core/fin-ops/get-started/one-version.md)を参照してください。

### <a name="cloud-components"></a>クラウド コンポーネント

顧客は、次のコンポーネントに対して最大で 3 回連続して更新の一時停止が可能です。 (3 回の更新は、約 6 磨月に対応しています。)

- コマースの本部および Finance and Operationsアプリ
- Commerce Scale Unit (クラウド自己ホスト)
- Commerce SDK および関連するローカル サイト コンフィギュレーション (モジュール、データア クション、テーマなど)

たとえば、現在バージョン 10.0.2 を使用している顧客は、バージョン10.0.3、10.0.4、および 10.0.5 に対する更新を一時停止できます。 ただし、バージョン 10.0.6 に更新する必要があります。 このシナリオでは、バージョン 10.0.7 が使用可能になると、バージョン 10.0.2 はサポートされなくなります。

### <a name="in-store-components"></a>ストア内のコンポーネント

顧客は、次のコンポーネントに対して最大で 7 回連続して更新の一時停止が可能です。 (7 回の更新は、約 12 磨月に対応しています。)

- Commerce Scale Unit (ストア内でホスト)
- Modern POS
- ハードウェア ステーション

たとえば、現在バージョン 10.0.2 を使用している顧客は、バージョン10.0.3 から 10.0.9 に対する更新を一時停止できます。 ただし、バージョン 10.0.10 に更新する必要があります。 このシナリオでは、バージョン 10.0.11 が使用可能になると、バージョン 10.0.2 はサポートされなくなります。

## <a name="additional-resources"></a>追加リソース

### <a name="one-version-service-updates"></a>One Version のサービス更新

1 つのバージョン サービスの更新詳細は、次のリソースをご覧ください。

- [1 つのバージョンのサービス更新に関するよく寄せられる質問](../fin-ops-core/fin-ops/get-started/one-version.md)
- [Dynamics 365 の更新方法を近代化](https://cloudblogs.microsoft.com/dynamics365/bdm/2018/07/06/modernizing-the-way-we-update-dynamics-365/)
- [Finance and Operations アプリの新しい柔軟なサービスを更新](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/06/03/new-flexible-service-updates-for-dynamics-365-for-finance-and-operations/)

### <a name="component-selection"></a>コンポーネントの選択

ニーズに合った適切なコンポーネントを選択する方法については、次のトピックを参照してください。

- [ストア内トポロジの選択](./dev-itpro/retail-in-store-topology.md)
- [Modern POS (MPOS) か Cloud POS (CPOS) かの選択](mpos-or-cpos.md)

### <a name="servicing-instructions"></a>サービスの手順

このトピックで説明されている個々のコンポーネントをサービスする方法については、次のトピックを参照してください。

- [Commerce Scale Unit のコンフィギュレーションとインストール](./dev-itpro/retail-store-scale-unit-configuration-installation.md)
- [更新プログラムの適用および Retail Cloud Scale Unit への拡張機能](../fin-ops-core/dev-itpro/deployment/update-retail-channel.md)
- [Modern POS (MPOS) のコンフィギュレーション、インストール、および有効にする](retail-modern-pos-device-activation.md)
- [Retail Hardware Station のコンフィギュレーションおよびインストール](retail-hardware-station-configuration-installation.md)
- [パッケージ コンフィギュレーションとオンライン チャネルへの配置](./e-commerce-extensibility/package-deploy.md)

### <a name="extensibility-and-packing"></a>拡張性および梱包

拡張機能の保守機能については、[配置可能なパッケージの作成](./dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。
