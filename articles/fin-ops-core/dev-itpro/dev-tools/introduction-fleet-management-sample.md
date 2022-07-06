---
title: フリート管理のサンプル アプリケーション
description: この記事は、フリート管理のサンプル アプリケーションについての概要です。
author: RobinARH
ms.date: 06/20/2017
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.custom: intro-internal
ms.assetid: 999b43b2-f149-4145-9d85-e2a62cd8da1e
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3791acb6ffd0f6d87651eebd89f86b925ae9ddc7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867057"
---
# <a name="fleet-management-sample-application"></a>フリート管理のサンプル アプリケーション

[!include [banner](../includes/banner.md)]

この記事は、フリート管理のサンプル アプリケーションについての概要です。

フリート管理サンプル アプリケーションは、開発および基板機能を示すために用意されています。 フリート管理は、ISV が車のレンタル機関用に作成するかもしれないソリューションを表します。 フリート管理データには、レンタルに使用できる車両、レンタルしてこれらの車両を戻すことができる顧客が含まれます。 従業員は、車両でメンテナンス ワークフローを実行することもできます。

一部のチュートリアルについては、コンピュータにない場合、FleetManagement ソリューションを作成する必要があります。 作成手順は「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。

一部のチュートリアルについては、フリート管理チュートリアル コードおよび <https://github.com/Microsoft/FMLab> から他のコンポーネントをダウンロードする必要があります。

フリート管理は、以下のようにプラットフォーム機能を示す Visual Studio ソリューションとして提供されます。

-   フォーム
-   ワークフロー
-   セキュリティ
-   ラベル
-   リソース
-   データ
-   ビジネス インテリジェンス
-   拡張子

フリート管理ソリューションには、2 つの独立したプロジェクト (基本モデル用のプロジェクトと、基本モデルに拡張するためのプロジェクト)。 FleetManagement Migrated という名前のプロジェクトは、Dynamics AX 2012 からコードを移行した後に、移行されたアプリケーションがどのように表示されるかを示しています。 このバージョンでは、Microsoft Dynamics AX 2012 R3 から移行されたフォームが Web クライアント上でどのように動作するかが示されます。 これらのフォームは、自動化された移行ツールおよび Visual Studio でのその他の手動移行手順を使用して作成されています。 これらのフォームは X++ テーブルにバインドし、X++ プログラミング モデルを使用します。 FleetManagement Discounts (または FleetManagementExtension) という名前のプロジェクトは、拡張子を使用してアプリケーションをカスタマイズする方法を示しています。 このプロジェクトは、コントロールとテーブルを拡張し、データイ ベントを処理し、プラグインを使用してビジネス ロジックを置き換えることで、フリート管理のサンプルを拡張します。 この記事に添付されているチュートリアルでは、Fleet Management のサンプルを詳しく見ていきます。 これらには、フリート管理のチュートリアル [フリート管理のサンプル アプリケーションのためのエンド ツー エンドのシナリオ](fleet-management-sample.md)、拡張機能を説明するチュートリアル、 [拡張機能によるモデル要素のカスタマイズ](../extensibility/customize-model-elements-extensions.md) が含まれます。

## <a name="additional-resources"></a>追加リソース

[フリート管理のサンプルを使用する](fleet-management-sample.md)

[拡張機能を使用してモデル要素をカスタマイズする](../extensibility/customize-model-elements-extensions.md)

[開発およびカスタマイズのホーム ページ](developer-home-page.md)

[FMLab サンプル コードをダウンロードする](https://github.com/Microsoft/FMLab)

[FleetManagement ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]