---
title: Dynamics 365 Commerce の削除済みまたは推奨されない機能
description: このトピックでは、Dynamics 365 Commerce から削除された、または削除される予定の機能について説明します。
author: josaw
ms.date: 04/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 213ed2091b1f2359f2481b162cba07812b3ffe90
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649078"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Dynamics 365 Commerce の削除済みまたは推奨されない機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Commerce から削除された、または削除される予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。 

> [!NOTE]
> 財務と運用アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](/dynamics/s-e/) を参照してください。 これら異なるバージョンのレポートを比較し、財務と運用アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。

## <a name="features-removed-or-deprecated-in-the-commerce-10025-release"></a>Commerce 10.0.25 リリースの削除済みまたは非推奨の機能

### <a name="modern-point-of-sale-mpos"></a>Modern 販売時点管理 (MPOS)

モダン販売時点管理 (MPOS) アプリケーションは、Commerce バージョン 10.0.25 のリリースで非推奨となり、Store Commerce アプリに置き換えらます。

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 店舗内のアプリは、Dynamics 365 Commerce オムニチャネル オファリングの基礎です。 モダンでインテリジェントなストア エクスペリエンスを提供するために継続的に革新し、Windows で既存の店舗内アプリケーションを使用し IT オペレーションとユーザー エクスペリエンスを大幅に改善する新しい一連の変更を展開するソリューションをさらにモダンにします。 新しい Store Commerce アプリケーションは、既存の MPOS のテクノロジ アップグレードです。 Windows プラットフォームでのパフォーマンス、信頼性、および長期のサポートを強化し、更新を行うごとにアプリを再梱包する必要がなされます。 |
| **別の機能で置き換えられているか?**   |  [Store Commerce](../dev-itpro/store-commerce.md) |
| **影響を受ける製品領域**         | Modern 販売時点管理 |
| **配置オプション**              | すべて |
| **状態**                         | 非推奨: Commerce バージョン 10.0.25 のリリース時に、LCS 仮想マシン (VMs) を介して出荷された MPOS インストーラーは、2023 年 10 月に削除されます。 |

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Commerce 10.0.21 リリースの削除済みまたは非推奨の機能

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>Commerce パラメーターでの重複割引処理の設定

**Commerce パラメーター** ページの **重複割引処理** 設定は、Commerce バージョン 10.0.21 のリリースで非推奨になりました。 今後、Commerce 価格決定エンジンは単一のアルゴリズムを使用して、重複する割引の最適な組み合わせを決定します。

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | <p>Commerce パラメーターの **重複割引処理** の設定は、Commerce の価格設定エンジンがどのように重複する割引の最適な組み合わせを検索および決定するかを制御します。 現在、次の 3 つのオプションがあります:<p><ul><li> **最適なパフォーマンス** – このオプションは、高度なヒューリスティック アルゴリズムと [基準額のランキング](../optimal-combination-overlapping-discounts.md) の方法を使用して、最適な割引の組み合わせを適切な方法で優先順位付け、評価、および決定します。</li><li>**バランス計算** – 現在のコード ベースでは、このオプションは **最適なパフォーマンス** オプションと同様に機能します。 したがって、これは基本的に重複したオプションです。</li><li>**包括的な計算** – このオプションでは、価格計算中にすべての可能な割引の組み合わせを調べる古いアルゴリズムを使用します。 このオプションは、明細行と数量が大きい注文では、パフォーマンス上の問題が発生する可能性があります。</li></ul><p>設定を簡素化し、パフォーマンスを向上させ、古いアルゴリズムによって発生するインシデントを削減するために、**重複割引処理** の設定を完全に削除し、 Commerce の価格設定エンジンの内部ロジックを更新して、高度なアルゴリズム (つまり、**最適なパフォーマンス** オプションのアルゴリズム) のみを使用するようにします。</p> |
| **別の機能で置き換えられているか?**   | いいえ。 この機能を削除する前に、**バランス計算** または **包括的な計算** オプションを使用している組織では、**最適なパフォーマンス** オプションに切り替えることをお勧めします。 |
| **影響を受ける製品領域**         | 価格決定と割引 |
| **配置オプション**              | すべて |
| **状態**                         | 10.0.21 リリースでは、2022 年 10 月に **重複割引処理** の設定が Commerce パラメーターから削除されます。 |

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>Lifecycle Services を使用して配布された Retail SDK

Retail SDKはLifecycle Services (LCS) に出荷されます。 この配布モードは、リリース 10.0.21 では非推奨になりました。 今後、Retail SDK 参照パッケージ、ライブラリ、およびサンプルは、GitHub の公開レポジトリで公開されます。

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | Retail SDK は LCS に出荷されます。 LCS プロセスは完了するのに数時間かかり、更新の度にプロセスを繰り返す必要があります。 今後、Retail SDK 参照パッケージ、ライブラリ、およびサンプルは、GitHub の公開レポジトリで公開されます。 拡張子サンプルおよび参照パッケージは簡単に消費され、更新は数分で完了します。 |
| **別の機能で置き換えられているか?**   |  [GitHub と NuGet から Retail SDK サンプルと参照パッケージをダウンロードする](../dev-itpro/retail-sdk/sdk-github.md) |
| **影響を受ける製品領域**         | Retail SDK |
| **配置オプション**              | All |
| **状態**                         | 非推奨: 10.0.21 のリリース現在、LCS VMs を介して出荷された SDK は、2023 年 10 月に削除されます。 |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>小売展開可能パッケージと、結合された POS、ハードウェア ステーション、および Cloud スケール ユニット インストーラー

Retail SDK MSBuild を使用して生成された小売展開可能パッケージは、10.0.21 で非推奨になりました。 今後、Cloud スケール ユニット拡張機能 (Commerce Runtime、チャンネル データベース、ヘッドレス コマース API、支払、および Cloud Point of Sale (POS)) の Cloud Scale Unit (CSU) パッケージを使用します。 POS、ハードウェア ステーション、および Cloud スケール ユニットの自己ホストには、拡張機能のインストーラーのみを使用します。

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 小売展開可能パッケージは、拡張機能パッケージとインストーラー完全なセットを含む結合パッケージです。 この結合パッケージは、CSU 拡張機能が Cloud スケール ユニットに移動し、インストーラーがストアに配置されるため、配置が複雑になります。 インストーラーには拡張機能と基本製品が含まれ、更新が困難です。 アップグレードごとに、コード マージとパッケージの生成が必要です。 このプロセスを簡略化するために、拡張機能パッケージはコンポーネントに分離され、配置と管理が容易になります。 新しいアプローチでは、拡張機能と基本製品のインストーラーが分離され、コード マージや再梱包を行わずに独立してサービスを提供および更新できます。|
| **別の機能で置き換えられているか?**   | CSU 拡張機能、POS 拡張機能インストーラー、ハードウェア ステーションの拡張機能インストーラー |
| **影響を受ける製品領域**         | Dynamics 365 Commerce 拡張機能と展開 |
| **配置オプション**              | All |
| **状態**                         | 非推奨: リリース 10.0.21 で、LCS の RetailDeployablePackage を配置するためのサポートは 2022 年 10 月に削除されます。 |

詳細については、以下を参照してください。

+ [Commerce Cloud Scale Unit (CSU) の個別パッケージの生成](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [Modern POS 拡張機能パッケージの作成](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [POS と新しいハードウェア デバイスの統合](../dev-itpro/hardware-device-extension.md)
+ Code サンプル
    + [Commerce Scale Unit](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [POS、CSU およびハードウェア ステーション](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>Retail SDK の ModernPos.Sln と CloudPos.sln

ModernPos.sln、CloudPos.sln、POS.Extension.csproj、および POS フォルダーを使用した POS 拡張機能開発は、リリース 10.0.21 では非推奨になりました。 今後は、POS の独立したパッケージ SDK を POS 拡張機能として使用します。

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | Retail SDK の以前のバージョンでは、POS 拡張機能がある場合、最新バージョンの POS に更新するため、コード マージと再梱包を行う必要がありました。 コード マージは時間のかかるアップグレード プロセスであり、Retail SDK 全体をリポジトリに維持する必要があります。 また、コア POS.App プロジェクトをコンパイルする必要があります。 独立したパッケージ モデルを使用して、拡張機能のみを維持する必要があります。 POS 拡張機能の最新バージョンに更新するプロセスは、プロジェクトで消費する NuGet パッケージのバージョン更新と同様に簡単です。 拡張機能は個別に配置でき、サービスは拡張機能インストーラーを使用します。 基準 POS は個別に配置および管理でき、基準インストーラーまたはコードとのコード マージや再梱包は必要ありません。 |
| **別の機能で置き換えられているか?**   | [POS の独立したパッケージ SDK](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **影響を受ける製品領域**         | Dynamics 365 Commerce POS 拡張機能と展開 |
| **配置オプション**              | All |
| **状態**                         | 非推奨: リリース 10.0.21 の時点で、Retail SDK の ModernPos.Sln、CloudPOs.sln、および POS.Extensons.csproj を使用する結合 POS パッケージと拡張モデルのサポートは、2023 年 10 月に削除される予定です。 |

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
| **廃止 / 削除の理由** | 2020 年 12 月より、すべての Dynamics 365 製品における Microsoft Internet Explorer 11 のサポートは非推奨になり、2021 年 8 月を過ぎると、Internet Explorer 11 はサポートされません。<br><br>これは、Internet Explorer 11 のインターフェイスを通じて使用されるように設計された Dynamics 365 製品を使用しているユーザーに影響します。 2021 年 8 月以降、そのような Dynamics 365 製品では Internet Explorer 11 はサポートされません。 |
| **別の機能で置き換えられているか?**   | Microsoft Edge に移行することをお勧めします。|
| **影響を受ける製品領域**         | すべての Dynamics 365 製品 |
| **配置オプション**              | すべて|
| **状態**                         | 非推奨。 2021 年 8 月を過ぎると、Internet Explorer 11 はサポートされません。|

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
