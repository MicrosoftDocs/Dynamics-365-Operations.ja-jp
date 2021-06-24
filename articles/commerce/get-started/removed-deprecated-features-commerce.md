---
title: Dynamics 365 Commerce の削除済みまたは推奨されない機能
description: このトピックでは、Dynamics 365 Commerce から削除された、または削除される予定の機能について説明します。
author: josaw
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: f80d1509c7c363e93b83cb47c1b93ab00bf67180
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193471"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Dynamics 365 Commerce の削除済みまたは推奨されない機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Commerce から削除された、または削除される予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。 

> [!NOTE]
> Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](/dynamics/s-e/)を参照してください。 これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Commerce 10.0.17 リリースの削除済みまたは非推奨の機能

### <a name="full-dataset-generation-interval-is-deprecated"></a>完全なデータセットの生成間隔は削除されます

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | このリリースから、 Dynamics 365 本部 の **Commerce Scheduler パラメーター** フォームでは、**日数の完全なデータセット生成間隔** は非推奨となります。 また、今回のリリースからは、フィールドを視覚的に削除し、値を編集できないようになっています。 これは **0** の値で表示されます。 |
| **別の機能で置き換えられているか?**   | なし |
| **影響を受ける製品領域**         | Dynamics 365 Commerce |
| **配置オプション**              | All|
| **状態**                         | 非推奨。 このフィールドを使用したり、値を変更したりすることはできません。|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Commerce 10.0.15 リリースの削除済みまたは非推奨の機能

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 による Internet Explorer 11 サポートの非推奨

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 2020 年 12 月より、すべての Dynamics 365 製品における Microsoft Internet Explorer 11 のサポートは非推奨になり、2021 年 8 月以降、Internet Explorer 11 はサポートされなくなります。<br><br>これは、Internet Explorer 11 のインターフェイスを通じて使用されるように設計された Dynamics 365 製品を使用しているユーザーに影響します。 2021 年 8 月以降、そのような Dynamics 365 製品では Internet Explorer 11 はサポートされません。 |
| **別の機能で置き換えられているか?**   | Microsoft Edge に移行することをお勧めします。|
| **影響を受ける製品領域**         | すべての Dynamics 365 製品 |
| **配置オプション**              | All|
| **ステータス**                         | 非推奨。 2021 年 8 月以降は、Internet Explorer 11 はサポートされません。|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Commerce 10.0.11 リリースの削除済みまたは非推奨の機能
### <a name="data-action-hooks"></a>データ アクションのフック
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | パフォーマンスの問題のために、データ アクション フック機能は廃止されました。 |
| **別の機能で置き換えられているか?**   | データアクション層のビジネス ロジックを変更するために、[データ アクションの上書き](../e-commerce-extensibility/data-action-overrides.md) の使用をお勧めします。|
| **影響を受ける製品領域**         | eコマースの拡張データ アクション |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: リリース 10.0.11 現在 |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Visual Studio 2015、msbuild 14.0、および Retail SDK\Reference ライブラリとツールのための Retail SDK サポート
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | Visual Studio 2015 の Retail SDK サポートは推奨されておらず、VS 2017、msbuild 15.0、すべての参照ライブラリをサポートするために更新され、RetailSDK\References フォルダ内の commerce プロキシ ジェネレーター ツールが、拡張モデルと SDK アップグレード プロセスを簡素化するために NuGet パッケージに移動しました。|
| **別の機能で置き換えられているか?**   | [Retail SDK を Visual Studio 2015 から Visual Studio 2017への移行](../dev-itpro/retail-sdk/migrate-sdk.md) の情報に従って、システムを更新することをお勧めします。 |
| **影響を受ける製品領域**         | Retail SDK 拡張機能 |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: リリース 10.0.11 現在 |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>IEdmModelExtender と CommerceController を使用した Retail Server 拡張機能
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | IEdmModelExtender と CommerceController を使用した Retail Server 拡張機能は、簡略化された拡張モデルを提供するために廃止されました。 新しい実装では、追加の IEdmModelExtender クラスの実装のない、コントローラー クラスのみが含まれます。 これにより、特定の OData バージョンとの依存関係を回避します (OData バージョンが更新されると、拡張機能が壊れてしまう可能性があります。) |
| **別の機能で置き換えられているか?**   |  NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) パッケージをインポートして、IController クラス拡張モデルを使用することをお勧めします。 |
| **影響を受ける製品領域**         | Retail Sever 拡張機能 |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: リリース 10.0.11 現在 |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>IHardwareStationController を使用した Hardware Station 拡張機能
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | IHardwareStationController を使用した Hardware Station 拡張機能は、簡略化された拡張モデルを提供するために廃止されました。 新しい実装では、追加のクラス実装のない、IController クラスのみを持つことになり、コア Hardware Station ライブラリとの依存関係を回避するために、以前の拡張では複数のライブラリを参照する必要があります。) |
| **別の機能で置き換えられているか?**   | NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) パッケージをインポートして、IController クラス拡張モデルを使用することをお勧めします。 |
| **影響を受ける製品領域**         | Hardware Station の拡張機能 |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: リリース 10.0.11 現在 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Commerce 10.0.10 リリースの削除済みまたは非推奨の機能
### <a name="pos-operation-803---picking-and-receiving"></a>POS operation 803 - ピッキングと入荷
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | ピッキングと入庫処理は、運用面の見直しに伴い、現在は使用されていません。 |
| **別の機能で置き換えられているか?**   | はい。 この機能は、インバウンド処理 (804) とアウトバウンド処理 (805) の 2 つの新しい POS 工程に置き換えられます。|
| **影響を受ける製品領域**         | 販売時点管理（POS）アプリケーション |
| **配置オプション**              | すべて |
| **ステータス**                         | 使用されていません：リリース 10.0.10 の時点で、ピッキングと入荷の処理は、新たな更新プログラムが適用されません。 今後のリリースでは、この処理に対する重大なバグの修正のみが行われます。 すべてのお客様には、新しい[インバウンド処理](../pos-inbound-inventory-operation.md)と[アウトバウンド処理](../pos-outbound-inventory-operation.md)への移行を奨励して おり、引き続き長期的な製品ロードマップに含まれています。 |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Commerce 10.0.7 リリースの削除済みまたは非推奨の機能
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities と GetAvailableInventoryNearby API
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | GetProductAvailabilities と GetAvailableInventoryNearby API は、新たに最適化された API に置き換えられます。 |
| **別の機能で置き換えられているか?**   | 今後は、GetEstimatedAvailabilty と GetEstimatedProductWarehouseAvailability API がご利用頂けます。 |
| **影響を受ける製品領域**         | eコマース アプリケーション SDK |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: リリース バージョン 10.0.7 の時点では、GetProductAvailabilities と GetAvailableInventoryNearby に対する新規開発は今後行われません。 これら API をeコマース環境で使用している組織では、新しい GetEstimatedAvailabilty と GetEstimatedProductWarehouseAvailability API に置き換えを行い、[最適化された商品在庫計算機能 ](../calculated-inventory-retail-channels.md) を有効化する必要があります。  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>削除済みまたは非推奨の機能に関する以前の発表
以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json)を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]