---
title: Dynamics 365 Commerce コンポーネントのバージョン管理要件
description: この記事では、Microsoft Dynamics 365 Commerce エコシステムのすべてのコンポーネントに対する、コンポーネント バージョン要件および依存関係の概要について説明します。
author: Reza-Assadi
ms.date: 10/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.11
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.search.form: RetailITWorkspace
ms.openlocfilehash: 627f3f443295971b199ccf5ef19ff584b700a902
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710690"
---
# <a name="dynamics-365-commerce-component-versioning-requirements"></a>Dynamics 365 Commerce コンポーネントのバージョン管理要件

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce エコシステムのすべてのコンポーネントに対する、コンポーネント バージョン要件および依存関係の概要について説明します。

次の図は、Dynamics 365 Commerce コンポーネントの概要、それに対応するバージョン要件および依存関係を示しています。

<a href="/dynamics365/commerce/media/commerce-component-versioning.jpg" target="_blank">![Dynamics 365 Commerce コンポーネント バージョン要件および依存関係。](./media/commerce-component-versioning.jpg)</a>

## <a name="component-dependencies"></a>コンポーネントの依存関係

### <a name="service-updates"></a>サービスの更新

顧客およびパートナーがサービスおよび配置を行うすべてのコマース コンポーネントとの互換性を確保するには、更新サービス中にいくつかのバージョン依存関係に従う必要があります。 次のリストは、これらの依存関係をすべて示しています。

- **Commerce headquarters および財務と運用アプリは、Commerce Scale Unit (クラウドと自己ホスト型の両方) と同じバージョンか、それ以降のバージョンである必要があります。**

    たとえば、Commerce headquarters および財務と運用アプリがバージョン 10.0.30 である場合、Commerce Scale Unit はバージョン 10.0.30 またはそれ以前 (10.0.29、または 10.0.28 など) である必要があります。

- **Commerce Scale Unit は、Modern Point of Sale (MPOS)、Hardware Station、コマース ソフトウェア キット (SDK) 以降のバージョン、および関連するローカル サイト コンフィギュレーション (モジュール、データ アクション、テーマなど) でなくてはなりません。**

    たとえば、Commerce Scale Unit がバージョン 10.0.30 である場合、Modern POS、Hardware Station、Commerce ストアフロントはバージョン 10.0.30 またはそれ以前 (たとえば、10.0.29 または 10.0.28) である必要があります。

- **拡張機能パッケージは、拡張機能が適用されるターゲット コンポーネントと同じバージョン、またはそれより以前のバージョンに対してコンパイルする必要があります。**

    たとえば、展開された Commerce Scale Unit がバージョン 10.0.30 である場合、対応する拡張パッケージをバージョン 10.0.30 またはそれ以前 (たとえば、10.0.29 または 10.0.28) に対してコンパイルする必要があります。

### <a name="quality-updates"></a>品質更新プログラム

品質更新プログラム中、サービス更新プログラムに必要なもの以外に、各コマース コンポーネントに対して特定のバージョン管理要件に従う必要はありません。

## <a name="current-supported-versions"></a>現在サポートされているバージョン

次のテーブルでは、**2022 年 10 月 21 日** 時点で、現在サポートされている各種 Commerce コンポーネントのバージョンを示します。

| コンポーネント | 利用可能な最新リリース (サンドボックス内の最初のリリース) | 利用可能な最新のコンポーネント バージョン番号 (サンドボックス内の最初のリリース) | サポートされている最も古いリリース | サポートされている最も古いコンポーネントのバージョン番号 |
|---|---|---|---|---|
| 財務と運用アプリ | 10.0.30 | 10.0.30 | 10.0.26 | 10.0.26 |
| Commerce Scale Unit (クラウド自己ホスト) | 10.0.30 | 9.40 | 10.0.30 | 9.36 |
| Commerce モジュール ライブラリ | 10.0.30 | 9.40 | 10.0.26 | 9.36 |
| Commerce Scale Unit (自己ホスト) | 10.0.30 | 9.40 | 10.0.22 | 9.32 |
| Modern POS | 10.0.30 | 9.40 | 10.0.22 | 9.32 |
| Hardware Station | 10.0.30 | 9.40 | 10.0.22 | 9.32 |

## <a name="one-version-requirements"></a>1 つのバージョン要求

Commerce コンポーネントは、1 つのバージョン サービスの更新をフォローします。 詳細については、[1 つのバージョン サービスに関してよく寄せられる質問](../fin-ops-core/fin-ops/get-started/one-version.md)を参照してください。

### <a name="cloud-components"></a>クラウド コンポーネント

顧客は、次のコンポーネントに対して最大で 3 回連続して更新の一時停止が可能です。 (3 回の更新は、約 6 磨月に対応しています。)

- Commerce headquarters および財務と運用アプリ
- Commerce Scale Unit (クラウド自己ホスト)
- Commerce SDK および関連するローカル サイト コンフィギュレーション (モジュール、データア クション、テーマなど)

たとえば、現在バージョン 10.0.30 を使用している顧客は、バージョン 10.0.31、10.0.32、10.0.33 に対する更新を一時停止できます。 ただし、バージョン 10.0.34 に更新する必要があります。 このシナリオでは、バージョン 10.0.35 が使用可能になると、バージョン 10.0.30 はサポートされなくなります。

### <a name="in-store-components"></a>ストア内のコンポーネント

顧客は、次のコンポーネントに対して最大で 7 回連続して更新の一時停止が可能です:
- Commerce Scale Unit (自己ホスト)
- Modern POS または Store Commerce
- ハードウェア ステーション

たとえば、現在バージョン 10.0.30 を使用している顧客は、リリースされたバージョン 10.0.31、10.0.32、10.0.33、10.0.34、10.0.35、10.0.36、10.0.37 に対する更新を一時停止できます。 ただし、バージョン 10.0.38 に更新する必要があります。 このシナリオでは、バージョン 10.0.38 が使用可能になると、バージョン 10.0.30 はサポートされなくなります。

## <a name="additional-resources"></a>追加リソース

### <a name="component-selection"></a>コンポーネントの選択

ニーズに合った適切なコンポーネントを選択する方法については、次の記事を参照してください:

- [ストア内トポロジの選択](./dev-itpro/retail-in-store-topology.md)
- [Modern POS (MPOS) か Cloud POS (CPOS) かの選択](mpos-or-cpos.md)

### <a name="servicing-instructions"></a>サービスの手順

この記事で説明されている個々のコンポーネントをサービスする方法については、次の記事を参照してください:

- [Commerce Scale Unit のコンフィギュレーションとインストール](./dev-itpro/retail-store-scale-unit-configuration-installation.md)
- [更新プログラムの適用および Retail Cloud Scale Unit への拡張機能](../fin-ops-core/dev-itpro/deployment/update-retail-channel.md)
- [Modern POS (MPOS) のコンフィギュレーション、インストール、および有効にする](retail-modern-pos-device-activation.md)
- [Retail Hardware Station のコンフィギュレーションおよびインストール](retail-hardware-station-configuration-installation.md)
- [パッケージ コンフィギュレーションとオンライン チャネルへの配置](./e-commerce-extensibility/package-deploy.md)

### <a name="extensibility-and-packing"></a>拡張性および梱包

拡張機能の保守機能については、[配置可能なパッケージの作成](./dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。


[!INCLUDE[footer-include](../includes/footer-banner.md)]

