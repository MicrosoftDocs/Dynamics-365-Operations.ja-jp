---
title: Modern POS (MPOS) および Cloud POS のデモ データ画面レイアウト
description: このトピックでは、Dynamics 365 Commerce の販売時点管理 (POS) のデモ データ セットに含まれている画面レイアウトに関する情報を提供します。
author: josaw1
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 935e1a550160515e2c325c39eab86be3b9fa5394
ms.sourcegitcommit: d82f319cf7dd26c93a3fd342de4fd537272fa8d2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2020
ms.locfileid: "4413909"
---
# <a name="demo-data-screen-layouts-in-modern-pos-mpos-and-cloud-pos"></a>Modern POS (MPOS) および Cloud POS のデモ データ画面レイアウト

[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 Commerce の販売時点管理 (POS) のデモ データ セットに含まれている画面レイアウトに関する情報を提供します。

## <a name="overview"></a>概要

Commerce のデモ データに含まれているサンプル画面レイアウトは、さまざまな小売セグメント、店員の役割、およびデバイスに最適化されたコンテンツを提供します。 1 つのレイアウトに複数のレイアウトサイズとボタングリッドの組み合わせを含めることで、店員によるデバイスとステーション間の移動を確実にカバーできます。 このトピックでは、これらのレイアウトの違いや、レイアウトが提供する操作や全体的なエクスペリエンスについて説明します。

![クロス デバイス デモ データのレイアウト](../commerce/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>画面レイアウト ID の構造

画面レイアウトを検索するには、**Retail と Commerce** \> **チャネル設定** \> **POS 設定** \> **POS** \> **画面レイアウト** の順に移動します。

![画面レイアウトのページ](../commerce/media/demo-screen-layouts-fig-2-1.png)

画面レイアウト ID は、最大 10 文字です。 ID は、次の 3 つの情報と順序で構成された文字列です。

1. 法人
2. レイアウトバージョン
3. 個人

### <a name="company"></a>法人

| 文字 | 法人         |
|--------|-----------------|
| A      | Adventure Works |
| F      | Fabrikam        |
| C      | Contoso         |

### <a name="layout-version"></a>レイアウトバージョン

| バージョン番号 | 説明                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | さまざまなデバイスや縦横比の複数の画面のサイズをサポートする基本バージョン |
| 3.1            | **お勧めの製品** パネル用の追加サポートのある基本バージョン        |
| 4              | 拡張された Fabrikam 更新版レイアウトの拡張バージョン                                  |

### <a name="persona"></a>個人

| 省略形 | 個人       | コンテンツ |
|--------------|---------------|----------|
| CSH          | 出納係       | レジ担当者のレイアウトには、顧客の注文、返品、割引、無効化、およびギフト カードなど、すべてのトランザクションに関連する工程が含まれます。 これらのレイアウトには、価格チェック、在庫検索、在庫数などの在庫管理の毎日のタスクも含まれます。 開始時金額、シフトの停止、タイム レコーダーなど基本的なシフト管理も提供されます。 |
| マネージャー          | 店長 | 店舗マネージャー レイアウトには、キャッシュレイアウトにあるすべてのトランザクションに関連する操作の他、税の上書きも含まれます。 また、これらのレイアウトには、価格チェック、在庫検索、在庫数などの在庫管理の毎日のタスクも含まれます。 シフトの開始、停止、終了のためのシフト管理が提供されます。 さらに、レイアウトには、入力、削除、支払/入金申告、金庫や銀行預金の引き出し操作が含まれます。 最後に、これらのレイアウトにはパフォーマンスレポートへのアクセスが含まれ、XおよびZレポートを印刷できます。 |
| STK          | 在庫係   | 在庫係レイアウトは、在庫管理のために最適化されています。 価格チェック、在庫検索、ピッキングと入荷、在庫数確認、キット分解などの日常業務へのアクセスが含まれています。 これらのレイアウトは、タイム レコーダー、シフトの停止などの基本的なシフト操作も提供します。 これらのレイアウトは、主にバックオフィスタスクを対象としていますが、在庫担当者はトランザクションの画面のレジ担当者と同じ操作をしています。 |

### <a name="example-layout"></a>レイアウトの例

これは、Fabrikam 社の、レイアウトバージョン 4、店長個人の画面レイアウト ID の例です。

F4MGR

次の図は、Fabrikam 店長のようこそ画面の例を示しています。

![Fabrikam 店長のようこそ画面](../commerce/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a>レイアウト サイズ

### <a name="full-vs-compact-layouts"></a>圧縮レイアウト対完全

画面レイアウトには、フルデバイスとコンパクトデバイスの両方のコンフィギュレーションを持つことができます。 したがって、ユーザーは、1 つの画面レイアウトに割り当てられ、さまざまなサイズとフォーム係数を店舗内で使用できます。

- **Modern POS - Full** - 通常、フル レイアウトは PC モニタまたはタブレットなどの大型ディスプレイに最適です。 ユーザーは、レイアウトに含まれる UI 要素を選択し、要素のサイズと配置を指定し、詳細なプロパティを設定できます。 フル レイアウトは、縦向きおよび横向きの両方のコンフィギュレーションをサポートします。
- **Modern POS - Compact** - コンパクトなレイアウトは、通常、携帯電話や小型タブレットに最適です。 コンパクト デバイスでは、設計の可能性が限られています。 ユーザーは、領収書ウインドウおよび合計ウインドウの列とフィールドをコンフィギュレーションできます。

### <a name="screen-resolutions-that-are-provided"></a>提供される画面解像度

次の表は、標準的な画面解像度で提供されているレイアウト サイズを示しています。

| レイアウト タイプ | 解像度 | 縦横比 | ターゲット表示          |
|-------------|------------|--------------|-------------------------|
| 最適化\*   | 480 × 853  | 16:9         | 電話                  |
| 完全        | 1024 × 768 | 4:3          | タブレット                 |
| 完全\*      | 1280 × 720 | 16:9         | タブレット                 |
| 完全        | 1366 × 768 | 16:9         | タブレット、大きい画面 |
| 完全        | 1440 × 960 | 3:2          | タブレット、大きい画面 |
| 完全\*      | 1536 × 864 | 16:9         | タブレット、大きい画面 |

\*これらの追加レイアウト サイズは、Adventure WorksとFabrikamレイアウトでのみ使用できます。

> [!TIP]
> POSでは、現在のアプリケーション ウィンドウの画面解像度に使用される最も近いサイズに基づいて、レイアウトのサイズが自動的に選択されます。 Modern POS (MPOS) または Retail Cloud POS (CPOS) で、現在使用されている画面レイアウト ID とレイアウトの解像度を知るには、**設定** ページを開き、**セッション情報** セクションを見ます。 現在のアプリケーションまたはブラウザーのフレームの実際のウィンドウの解像度を表示することもできます。 この情報を得た後に、**チャネル設定** \> **POS 設定** \> **POS** \> **画面レイアウト** で、レイアウト コンテンツのソースを検索することができます。

![Commerce と POS での画面レイアウトとレイアウトの解像度/サイズ](../commerce/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>会社およびブランド

各架空の会社では、さまざまな小売セグメントを対象としており、会社の市場用に調整された製品カタログが含まれています。 各企業は、その製品に付属する独自のビジュアルブランドを持っています。 ブランド要素には、アクセントの色、濃いまたは薄いテーマ、およびエクスペリエンスを提供する付属の写真が含まれます。

### <a name="company-segment-and-visual-characteristics"></a>会社のセグメントと視覚的な特性

| 法人         | 保管場所 | 区分        | アクセント | テーマ |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | シアトル  | スポーツ用品 | 青   | 濃い色  |
| Fabrikam        | サンフランシスコ  | ファッション        | 緑  | 薄い色 |
| Contoso         | ボストン   | 電子    | 赤    | 濃い色  |

> [!NOTE]
> Adventure WorksとFabrikamは、2つの主要ブランドです。 Contoso は使用可能ですが、すべてのレイアウトが提供されているわけではありません。

次の図は、3つの架空企業のようこそページとトランザクション ページの例を示しています。

### <a name="adventure-works"></a>Adventure Works

![Adventure Works のデモ データ ウェルカムページ](../commerce/media/demo-screen-layouts-fig-4-1a.png)

![Adventure Works のデモ データ トランザクションページ](../commerce/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![Fabrikam のデモ データ ウェルカムページ](../commerce/media/demo-screen-layouts-fig-4-2a.png)

![Fabrikam のデモ データ トランザクション](../commerce/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>Contoso

![Contosoのデモ データのレイアウト](../commerce/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>ユーザー ログ イン マトリックス

ユーザーには、さまざまな画面レイアウトが提供されています。 次の表を使用すると、どの画面にもアクセスできます。 適切な演算子 ID を使用してログインします。

| 法人         | 画面レイアウト ID | 個人       | オペレーター ID           |
|-----------------|------------------|---------------|------------------------|
| Adventure Works | A3MGR            | 店長 | 000154, 000137, 000073 |
| Adventure Works | A3CSH            | 出納係       | 000150, 000175, 000165 |
| Adventure Works | A3STK            | 在庫係   | 000155, 000181, 000152 |
| Fabrikam        | F4MGR            | 店長 | 000160、000713         |
| Fabrikam        | F3CSH            | 出納係       | 000161, 000113, 000114 |
| Fabrikam        | F3STK            | 在庫係   | 000164, 000112, 000123 |
| Contoso         | C3MGR            | 店長 | 000100, 000111         |
| Contoso         | C3CSH            | 出納係       | 000110, 000120         |
| Contoso         | 適用できません   | 在庫係   | 適用できません         |

> [!TIP]
> 最適な結果を得るには、対応する店舗在庫場所で登録を有効にし、ログインしたときに使用するペルソナの会社に会社を設定します。 これにより、エクスペリエンス全体で、視覚プロファイルやブランド イメージを合わせることができます。 たとえば、レジ担当者用の Fabrikam レイアウトを表示する場合、ヒューストンストアのレジスターを有効にする必要があります。

<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail and Commerce \> Channel setup \> POS setup \> POS \> Images**. -->

<!-- ![Images in Dynamics 365 Commerce](../commerce/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../commerce/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->
